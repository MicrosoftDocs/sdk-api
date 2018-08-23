---
UID: NS:ntsecpkg._SECPKG_USER_FUNCTION_TABLE
title: "_SECPKG_USER_FUNCTION_TABLE"
author: windows-sdk-content
description: The SECPKG_USER_FUNCTION_TABLE structure contains pointers to the functions that a security package implements to support executing in process with client/server applications. This structure is provided by the SpUserModeInitialize function.
old-location: security\secpkg_user_function_table.htm
old-project: secauthn
ms.assetid: 2b3fc6d1-2f55-4053-9271-f5cb5c318555
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PSECPKG_USER_FUNCTION_TABLE, PSECPKG_USER_FUNCTION_TABLE, PSECPKG_USER_FUNCTION_TABLE structure pointer [Security], SECPKG_USER_FUNCTION_TABLE, SECPKG_USER_FUNCTION_TABLE structure [Security], _SECPKG_USER_FUNCTION_TABLE, _ssp_secpkg_user_function_table, ntsecpkg/PSECPKG_USER_FUNCTION_TABLE, ntsecpkg/SECPKG_USER_FUNCTION_TABLE, security.secpkg_user_function_table"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SECPKG_USER_FUNCTION_TABLE, *PSECPKG_USER_FUNCTION_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - SECPKG_USER_FUNCTION_TABLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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
					

