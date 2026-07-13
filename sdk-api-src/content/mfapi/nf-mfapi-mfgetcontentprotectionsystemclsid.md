---
UID: NF:mfapi.MFGetContentProtectionSystemCLSID
title: MFGetContentProtectionSystemCLSID function (mfapi.h)
description: Gets the class identifier for a content protection system.
helpviewer_keywords: ["MFGetContentProtectionSystemCLSID","MFGetContentProtectionSystemCLSID function [Media Foundation]","mf.mfgetcontentprotectionsystemclsid","mfapi/MFGetContentProtectionSystemCLSID"]
old-location: mf\mfgetcontentprotectionsystemclsid.htm
tech.root: mf
ms.assetid: 03E1AF8D-69C7-4988-A699-0BD71ED635AF
ms.date: 12/05/2018
ms.keywords: MFGetContentProtectionSystemCLSID, MFGetContentProtectionSystemCLSID function [Media Foundation], mf.mfgetcontentprotectionsystemclsid, mfapi/MFGetContentProtectionSystemCLSID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFGetContentProtectionSystemCLSID
 - mfapi/MFGetContentProtectionSystemCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFGetContentProtectionSystemCLSID
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The class identifier can be used to create the input trust authority (ITA) for the content protection system. Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> or <a href="/windows/desktop/api/mfidl/nf-mfidl-imfpmphost-createobjectbyclsid">IMFPMPHost::CreateObjectByCLSID</a> to get an <a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedinput">IMFTrustedInput</a>  pointer.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>