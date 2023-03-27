# FaceTec SDK
The FaceTec SDK is a facial recognition software development kit that provides a secure and user-friendly way to authenticate users. The SDK uses 3D Face Authentication to verify user identity, which provides a high level of security and eliminates the need for passwords or other traditional authentication methods.

The FaceTec SDK can be used in a variety of industries, including banking, healthcare, e-commerce, and more. It can be integrated into mobile apps, web applications, and desktop software to provide secure and easy-to-use authentication solutions.

## Features
The FaceTec SDK includes a variety of features that make it a powerful and user-friendly authentication solution:

- 3D Face Authentication: The SDK uses 3D Face Authentication to verify user identity, which provides a high level of security and eliminates the need for passwords or other traditional authentication methods.
- Liveness Detection: The SDK includes liveness detection to prevent fraud by ensuring that the person being authenticated is physically present and not a photograph or video.
- User Feedback: The SDK provides user feedback during the authentication process to ensure that users are properly positioned and lit for optimal facial recognition.
- Seamless Integration: The SDK is easy to integrate into mobile apps, web applications, and desktop software.
### Integration
- To integrate the FaceTec SDK into your application, you must register on the FaceTec website and obtain the necessary credentials to use the SDK. Once you have the credentials, you can integrate the SDK into your app using the documentation and code examples provided by FaceTec.

# Facetec Response Documentation

This document explains the structure of the response object returned by the Facetec API.

- `"_id"`: Unique ID of the response object.
- `"idScanAgeEstimateGroupEnumInt"`: Age group.
- `"externalDatabaseRefID"`: Tuple reference.
- `"matchLevel"`: Match level. See more at https://dev.facetec.com/matching-guide.
- `"fullIDStatusEnumInt"`: Full ID status. 0 = FULL_ID_DETECTED, 1 = COULD_NOT_CONFIDENTLY_DETERMINE_FULL_ID_USER_NEEDS_TO_RETRY.
- `"digitalIDSpoofStatusEnumInt"`: Digital ID spoof status. 0 = LIKELY_PHYSICAL_ID, 1 = COULD_NOT_CONFIDENTLY_DETERMINE_PHYSICAL_ID_USER_NEEDS_TO_RETRY.
- `"scanResultBlob"`: Unused in this collection.
- `"nfcStatusEnumInt"`: NFC status. 0 = NO_NFC_SPECIFIED_BY_TEMPLATE, 1 = NFC_REQUESTED_BUT_DEVICE_NOT_CAPABLE, 2 = NFC_REQUESTED_BUT_USER_PRESSED_SKIP, 3 = NFC_REQUESTED_BUT_ERROR_ACCESSING_CHIP, 4 = SUCCESS.
- `"barcodeStatusEnumInt"`: Barcode status. 0 = NO_BARCODE_SPECIFIED_BY_TEMPLATE, 1 = BARCODE_REQUESTED_BUT_NOT_FOUND, 2 = BARCODE_REQUESTED_BUT_ERROR_READING, 3 = SUCCESS.
- `"faceOnDocumentStatusEnumInt"`: Face on document status. 0 = NOT_AVAILABLE, 1 = LIKELY_ORIGINAL_FACE, 2 = CANNOT_CONFIRM_ID_IS_AUTHENTIC.
- `"textOnDocumentStatusEnumInt"`: Text on document status. 0 = NOT_AVAILABLE, 1 = LIKELY_ORIGINAL_TEXT, 2 = CANNOT_CONFIRM_ID_IS_AUTHENTIC.
- `"matchLevelNFCToFaceMap"`: Match level.
- `"success"`: Result of the transaction.
- `"wasProcessed"`: Transaction was processed.
- `"callData"`: Call data object.
  - `"tid"`: Transaction ID.
  - `"path"`: Endpoint.
  - `"date"`: Date.
  - `"epochSecond"`: Epoch time.
  - `"requestMethod"`: Method type.
- `"additionalSessionData"`: Additional session data object.
  - `"isAdditionalDataPartiallyIncomplete"`: Is data incomplete.
  - `"platform"`: OS device.
  - `"appID"`: App ID.
  - `"installationID"`: Installation ID.
  - `"deviceModel"`: Device model.
  - `"deviceSDKVersion"`: SDK version.
  - `"sessionID"`: Session ID.
  - `"userAgent"`: User agent.
  - `"ipAddress"`: IP address.
- `"error"`: Error status.

### Server Info

- `coreServerSDKVersion`: The version of the SDK core.
- `customOrStandardServerSDKVersion`: The version of the SDK.
- `type`: The type of server.
- `mode`: The mode of the server.

### Data

- `idScan`: The ID of the scan.
- `idScanFrontImage`: The ID of the front image.
- `idScanBackImage`: The ID of the back image.
- `photoIDBackCrop`: The ID of the back crop.
- `photoIDFrontCrop`: The ID of the front crop.
- `photoIDFaceCrop`: The ID of the face crop.
- `photoIDPrimarySignatureCrop`: The ID of the primary signature crop.
- `photoIDSecondarySignatureCrop`: The ID of the secondary signature crop (if it exists).
- `extractedNFCImage`: The NFC image.
- `autoExtractedOCRData`: An object containing the following fields:
  - `firstName`: The first name.
  - `lastName`: The last name.
  - `dateOfExpiration`: The date of expiration of the ID.
  - `dateOfIssue`: The date of issue of the ID.
  - `dateOfBirth`: The date of birth.
  - `middleName`: The middle name.
  - `idNumber`: The ID number.
- `templateInfo`: An object containing the following fields:
  - `templateName`: The name of the template used.
  - `templateType`: The type of the template.
- `photoIDTamperingEvidenceFrontImage`: The ID of the front image used for tampering evidence.
- `photoIDTamperingEvidenceBackImage`: The ID of the back image used for tampering evidence.

### Enrollment Session

- `$oid`: The ID of the enrollment session.

### ID Scan Session ID

- The ID of the ID scan session.

#####  Facetec's answer in JSON format: A detailed look at biometric identification

![Image](https://github.com/mfs-victorlopezc/Documentacion-FaceTec/blob/main/response-data.png)
