---
UID: NF:mfapi.MFTUnregister
title: MFTUnregister function (mfapi.h)
author: windows-sdk-content
description: Unregisters a Media Foundation transform (MFT).
old-location: mf\mftunregister.htm
tech.root: medfound
ms.assetid: 2e63a098-5b83-4ea9-8149-4972f8ed0944
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 2e63a098-5b83-4ea9-8149-4972f8ed0944, MFTUnregister, MFTUnregister function [Media Foundation], mf.mftunregister, mfapi/MFTUnregister
ms.topic: function
f1_keywords: 
 - "mfapi/MFTUnregister"
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFTUnregister
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFTUnregister function


## -description


Unregisters a Media Foundation transform (MFT).
        


## -parameters




### -param clsidMFT [in]

The CLSID of the MFT.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function removes the registry entries created by the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

It is safe to call <b>MFTUnregister</b> twice with the same CLSID. If the CLSID is not found in the registry, the function succeeds and does nothing.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>
 

 

