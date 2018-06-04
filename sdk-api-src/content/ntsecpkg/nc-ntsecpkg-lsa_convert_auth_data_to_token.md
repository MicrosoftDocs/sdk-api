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

# LSA_CONVERT_AUTH_DATA_TO_TOKEN callback function


## -description


The <b>ConvertAuthDataToToken</b> function creates an access token from the authorization data returned from the 
<a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a> or 
<a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a> functions.


## -parameters




### -param UserAuthData [in]

Pointer to the authorization data received from the 
<a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a> or 
<a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a> functions.


### -param UserAuthDataSize [in]

Size, in bytes, of the authorization data specified by the <i>UserAuthData</i> parameter.


### -param ImpersonationLevel [in]

A 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> value specifying the impersonation level for the token to be created.


### -param TokenSource [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a> structure specifying the source to record in the token.


### -param LogonType [in]

A 
<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a> value indicating the type of logon to record in the token.


### -param AuthorityName [in]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that specifies the name of the authority that authorized this user, typically a domain name.


### -param Token [out]

Pointer to a HANDLE that receives the user token handle.

When you have finished using the user token, release the handle by calling <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.


### -param LogonId [out]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> that receives the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon identifier</a> for the token.


### -param AccountName [out]

Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> structure that receives the account name encoded in the <i>UserAuthData</i> parameter.


### -param SubStatus [out]

Pointer to a variable that receives additional information about the return value of the function call.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.




## -remarks



A pointer to the <b>ConvertAuthDataToToken</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1cc02c6b-2628-441d-97ae-ed83a4f6bfd0">GetAuthDataForUser</a>



<a href="https://msdn.microsoft.com/2436eaee-1f32-4e32-9a98-74968ad9b58e">GetUserAuthData</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/d775d782-9403-47b2-bb43-8f677db49eb9">SECURITY_LOGON_TYPE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a>
 

 

