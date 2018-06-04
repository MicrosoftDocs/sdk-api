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

# DRMGetOwnerLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetOwnerLicense</b> function retrieves an owner license created by calling the <a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a>.


## -parameters




### -param hIssuanceLicense [in]

A handle to a signed issuance license.


### -param puOwnerLicenseLength

TBD


### -param wszOwnerLicense [out]

A null-terminated string that contains the owner license in XrML format. For example XrML owner license, see <a href="https://msdn.microsoft.com/5c9ccaf3-e4ef-4b01-87f7-9c18cd3bc4d0">Owner License XML Example</a>.


#### - puLength [in, out]

An unsigned integer that contains the length, in characters, of the owner license retrieved by this function. The terminating null character is included in the length.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



An owner license is an end-user license that contains the OWNER right and allows the user to exercise all rights regardless of whether they are specifically granted. It is created by the AD RMS client when you call <a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a> and sign an issuance license offline.  If <b>DRMGetSignedIssuanceLicense</b> is called with the <i>uFlags</i> parameter set to <b>DRM_OWNER_LICENSE_NOPERSIST</b>, the owner license is saved in memory. Otherwise, it is saved in the license store. The <b>DRMGetOwnerLicense</b> function automatically retrieves the license from either location.




## -see-also




<a href="https://msdn.microsoft.com/3ed180d1-27c9-4f39-b353-1d417636ca62">DRMGetSignedIssuanceLicense</a>
 

 

