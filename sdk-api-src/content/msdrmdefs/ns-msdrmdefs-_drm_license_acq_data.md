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

# _DRM_LICENSE_ACQ_DATA structure


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

Not supported.

The <b>DRM_LICENSE_ACQ_DATA</b> structure holds license acquisition data during nonsilent license acquisition.
<div class="alert"><b>Note</b>  Nonsilent license acquisition is supported only in Rights Management Services client 1.0. Effective with RMS client 1.0 SP1, nonsilent license acquisition is no longer supported.</div><div> </div>

## -struct-fields




### -field uVersion

Version of this structure, for backward compatibility. In C, this value should be initialized to <b>DRMLICENSEACQDATAVERSION</b>.


### -field wszURL

URL of a license-granting website.


### -field wszLocalFilename

The path and file name of a local HTML file that will automatically send a license request when loaded in a browser.


### -field pbPostData

Pointer to a URL-safe base64-encoded string containing the license request.


### -field dwPostDataSize

The post data size in characters, plus one for a null terminator.


### -field wszFriendlyName

A human-readable name for the license-granting website.


## -remarks



This structure has a C++ default constructor that takes no parameters and sets all members to <b>NULL</b>, except <b>uVersion</b>, which is set to <b>DRMLICENSEACQDATAVERSION</b>.




## -see-also




<a href="https://msdn.microsoft.com/06a0c6d2-108d-4c72-9ae6-8959304602c5">AD RMS Structures</a>



<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>
 

 

