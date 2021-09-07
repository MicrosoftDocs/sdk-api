---
UID: NF:mfapi.MFTUnregister
title: MFTUnregister function (mfapi.h)
description: Unregisters a Media Foundation transform (MFT).
helpviewer_keywords: ["2e63a098-5b83-4ea9-8149-4972f8ed0944","MFTUnregister","MFTUnregister function [Media Foundation]","mf.mftunregister","mfapi/MFTUnregister"]
old-location: mf\mftunregister.htm
tech.root: mf
ms.assetid: 2e63a098-5b83-4ea9-8149-4972f8ed0944
ms.date: 12/05/2018
ms.keywords: 2e63a098-5b83-4ea9-8149-4972f8ed0944, MFTUnregister, MFTUnregister function [Media Foundation], mf.mftunregister, mfapi/MFTUnregister
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFTUnregister
 - mfapi/MFTUnregister
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
 - MFTUnregister
---

# MFTUnregister function


## -description

Unregisters a Media Foundation transform (MFT).

## -parameters

### -param clsidMFT [in]

The CLSID of the MFT.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function removes the registry entries created by the <a href="/windows/desktop/api/mfapi/nf-mfapi-mftregister">MFTRegister</a> function.

It is safe to call <b>MFTUnregister</b> twice with the same CLSID. If the CLSID is not found in the registry, the function succeeds and does nothing.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/media-foundation-transforms">Media Foundation Transforms</a>