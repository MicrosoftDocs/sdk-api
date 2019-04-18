---
UID: NS:msdrmdefs._DRM_LICENSE_ACQ_DATA
title: DRM_LICENSE_ACQ_DATA (msdrmdefs.h)
author: windows-sdk-content
description: Holds license acquisition data during nonsilent license acquisition.
old-location: rm\drm_license_acq_data.htm
tech.root: AdRms_Sdk
ms.assetid: c8f4ba99-5711-495f-9820-f604cc9e20f7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRM_LICENSE_ACQ_DATA, DRM_LICENSE_ACQ_DATA structure [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRM_LICENSE_ACQ_DATA, rm.drm_license_acq_data
ms.topic: struct
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRM_LICENSE_ACQ_DATA
product: Windows
targetos: Windows
req.typenames: DRM_LICENSE_ACQ_DATA
req.redist: 
req.product: Rights Management Services client 1.0 or later
ms.custom: 19H1
---

# DRM_LICENSE_ACQ_DATA structure


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


### -field _DRM_LICENSE_ACQ_DATA

TBD 




## -remarks



This structure has a C++ default constructor that takes no parameters and sets all members to <b>NULL</b>, except <b>uVersion</b>, which is set to <b>DRMLICENSEACQDATAVERSION</b>.




## -see-also




<a href="https://msdn.microsoft.com/06a0c6d2-108d-4c72-9ae6-8959304602c5">AD RMS Structures</a>



<a href="https://msdn.microsoft.com/0d4ce794-8384-4f1c-bc8c-1e67fbb5f987">DRMAcquireLicense</a>
 

 

