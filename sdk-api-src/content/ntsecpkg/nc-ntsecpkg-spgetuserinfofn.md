---
UID: NC:ntsecpkg.SpGetUserInfoFn
title: SpGetUserInfoFn
author: windows-sdk-content
description: Retrieves information about a logon session.
old-location: security\spgetuserinfo.htm
old-project: SecAuthN
ms.assetid: ee37fab0-5ee5-4cc5-9fcc-5c74cb0b2b26
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: NO_LONG_NAMES, SpGetUserInfo, SpGetUserInfo function [Security], SpGetUserInfoFn, UNDERSTANDS_LONG_NAMES, _ssp_spgetuserinfo, ntsecpkg/SpGetUserInfo, security.spgetuserinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpGetUserInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpGetUserInfoFn callback function


## -description


The <b>SpGetUserInfo</b> function retrieves information about a logon <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session</a>.


## -parameters




### -param LogonId [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> containing the logon session for which information is to be retrieved.


### -param Flags [in]

Specifies the acceptable length of the domain name as one of the following values. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NO_LONG_NAMES"></a><a id="no_long_names"></a><dl>
<dt><b>NO_LONG_NAMES</b></dt>
</dl>
</td>
<td width="60%">
The returned domain name cannot be longer than 15 characters.

</td>
</tr>
<tr>
<td width="40%"><a id="UNDERSTANDS_LONG_NAMES"></a><a id="understands_long_names"></a><dl>
<dt><b>UNDERSTANDS_LONG_NAMES</b></dt>
</dl>
</td>
<td width="60%">
The returned domain name can be longer than 15 characters.

</td>
</tr>
</table>
 


### -param *UserData [out]

Pointer to a pointer to a 
<a href="https://msdn.microsoft.com/1a56203a-ed6a-4f32-9e7c-b498ba61a64b">SecurityUserData</a> structure. If the function call succeeds, the user information is returned in this structure. The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> should allocate the memory for this structure in the caller's address space. The caller is responsible for freeing the buffer by calling the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <i>Flags</i> value NO_LONG_NAMES provides compatibility with Microsoft NTLM.

SSP/APs must implement the <b>SpGetUserInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetUserInfo</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

