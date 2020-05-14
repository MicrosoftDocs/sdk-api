---
UID: NF:mfidl.MFCreateSourceResolver
title: MFCreateSourceResolver function (mfidl.h)
description: Creates the source resolver, which is used to create a media source from a URL or byte stream.helpviewer_keywords: ["60d6b0e2-5ab2-4a20-99d9-e6b806a1f576","MFCreateSourceResolver","MFCreateSourceResolver function [Media Foundation]","mf.mfcreatesourceresolver","mfidl/MFCreateSourceResolver"]
old-location: mf\mfcreatesourceresolver.htm
tech.root: medfound
ms.assetid: 60d6b0e2-5ab2-4a20-99d9-e6b806a1f576
ms.date: 12/05/2018
ms.keywords: 60d6b0e2-5ab2-4a20-99d9-e6b806a1f576, MFCreateSourceResolver, MFCreateSourceResolver function [Media Foundation], mf.mfcreatesourceresolver, mfidl/MFCreateSourceResolver
f1_keywords:
- mfidl/MFCreateSourceResolver
dev_langs:
- c++
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
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
- MFCreateSourceResolver
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFCreateSourceResolver function


## -description


Creates the source resolver, which is used to create a media source from a URL or byte stream.
        


## -parameters




### -param ppISourceResolver [out]

Receives a pointer to the source resolver's <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver">IMFSourceResolver</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Note</b>  Prior to Windows 7, this function was exported from mf.dll. Starting in Windows 7, this function is exported from mfplat.dll, and mf.dll exports a stub function that calls into mfplat.dll. For more information, see <a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-headers-and-libraries">Library Changes in Windows 7</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/source-resolver">Source Resolver</a>
 

 

