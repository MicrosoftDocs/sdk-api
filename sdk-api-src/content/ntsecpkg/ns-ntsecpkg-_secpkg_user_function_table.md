---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SECPKG_USER_FUNCTION_TABLE structure


## -description



			The <b>SECPKG_USER_FUNCTION_TABLE</b> structure contains pointers to the functions that a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> implements to support executing in process with client/server applications. This structure is provided by the 
<a href="https://msdn.microsoft.com/e260db29-995b-4f32-b389-4ef62b3b29bc">SpUserModeInitialize</a> function.


## -struct-fields




### -field InstanceInit

Pointer to the <b>InstanceInit</b> function.
					


### -field InitUserModeContext

Pointer to the <b>InitUserModeContext</b> function.
					


### -field MakeSignature

Pointer to the <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> function.
					


### -field VerifySignature

Pointer to the <a href="https://msdn.microsoft.com/bebeef92-1d6e-4879-846f-12d706db0653">VerifySignature</a> function.
					


### -field SealMessage

Pointer to the <b>SealMessage</b> function.
					


### -field UnsealMessage

Pointer to the <b>UnsealMessage</b> function.
					


### -field GetContextToken

Pointer to the <b>GetContextToken</b> function.
					


### -field QueryContextAttributes

Pointer to the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.
					


### -field CompleteAuthToken

Pointer to the <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function.
					


### -field DeleteUserModeContext

Pointer to the <b>DeleteUserModeContext</b> function.
					


### -field FormatCredentials

Pointer to the <b>FormatCredentials</b> function.
					


### -field MarshallSupplementalCreds

Pointer to the <b>MarshallSupplementalCreds</b> function.
					


### -field ExportContext

Pointer to the <b>ExportContext</b> function.
					


### -field ImportContext

Pointer to the <b>ImportContext</b> function.
					

