---
UID: NC:ntsecpkg.SpGetUserInfoFn
title: SpGetUserInfoFn (ntsecpkg.h)
author: windows-sdk-content
description: Retrieves information about a logon session.
old-location: security\spgetuserinfo.htm
tech.root: SecAuthN
ms.assetid: ee37fab0-5ee5-4cc5-9fcc-5c74cb0b2b26
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NO_LONG_NAMES, SpGetUserInfo, SpGetUserInfo callback function [Security], SpGetUserInfoFn, SpGetUserInfoFn callback, UNDERSTANDS_LONG_NAMES, _ssp_spgetuserinfo, ntsecpkg/SpGetUserInfo, security.spgetuserinfo
ms.topic: callback
f1_keywords:
- ntsecpkg/SpGetUserInfo
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- Ntsecpkg.h
api_name:
- SpGetUserInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SpGetUserInfoFn callback function


## -description


The <b>SpGetUserInfo</b> function retrieves information about a logon <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">session</a>.


## -parameters




### -param LogonId [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">LUID</a> containing the logon session for which information is to be retrieved.


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
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-security_user_data">SecurityUserData</a> structure. If the function call succeeds, the user information is returned in this structure. The <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a> should allocate the memory for this structure in the caller's address space. The caller is responsible for freeing the buffer by calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function.


## -returns



If the function succeeds, return STATUS_SUCCESS.

If the function fails, return an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



The <i>Flags</i> value NO_LONG_NAMES provides compatibility with Microsoft NTLM.

SSP/APs must implement the <b>SpGetUserInfo</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpGetUserInfo</b> function is available in the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a>
 

 

