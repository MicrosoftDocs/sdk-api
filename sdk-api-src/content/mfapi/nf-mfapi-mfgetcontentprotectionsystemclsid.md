---
UID: NF:mfapi.MFGetContentProtectionSystemCLSID
title: MFGetContentProtectionSystemCLSID function
author: windows-sdk-content
description: Gets the class identifier for a content protection system.
old-location: mf\mfgetcontentprotectionsystemclsid.htm
tech.root: medfound
ms.assetid: 03E1AF8D-69C7-4988-A699-0BD71ED635AF
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFGetContentProtectionSystemCLSID, MFGetContentProtectionSystemCLSID function [Media Foundation], mf.mfgetcontentprotectionsystemclsid, mfapi/MFGetContentProtectionSystemCLSID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetContentProtectionSystemCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFGetContentProtectionSystemCLSID
: 
---

# MFGetContentProtectionSystemCLSID function


## -description


Gets the class identifier for a content protection system.


## -parameters




### -param guidProtectionSystemID [in]

The GUID that identifies the content protection system.


### -param pclsid [out]

Receives the class identifier to the content protection system.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The class identifier can be used to create the input trust authority (ITA) for the content protection system. Call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> or <a href="https://msdn.microsoft.com/787fc392-1858-41f4-a1ce-2da02a5e789f">IMFPMPHost::CreateObjectByCLSID</a> to get an <a href="https://msdn.microsoft.com/59a9def7-69a6-4f80-bb5e-1cb372ff6eab">IMFTrustedInput</a>  pointer.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

