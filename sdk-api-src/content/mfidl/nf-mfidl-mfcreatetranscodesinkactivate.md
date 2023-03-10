---
UID: NF:mfidl.MFCreateTranscodeSinkActivate
title: MFCreateTranscodeSinkActivate function (mfidl.h)
description: Creates the transcode sink activation object.
helpviewer_keywords: ["MFCreateTranscodeSinkActivate","MFCreateTranscodeSinkActivate function [Media Foundation]","mf.mfcreatetranscodesinkactivate","mfidl/MFCreateTranscodeSinkActivate"]
old-location: mf\mfcreatetranscodesinkactivate.htm
tech.root: mf
ms.assetid: cc9c604d-7f5a-4afb-a2df-b270ef883e68
ms.date: 12/05/2018
ms.keywords: MFCreateTranscodeSinkActivate, MFCreateTranscodeSinkActivate function [Media Foundation], mf.mfcreatetranscodesinkactivate, mfidl/MFCreateTranscodeSinkActivate
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateTranscodeSinkActivate
 - mfidl/MFCreateTranscodeSinkActivate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateTranscodeSinkActivate
---

# MFCreateTranscodeSinkActivate function


## -description

Creates the transcode sink activation object.

The transcode sink activation object can be used to create any of the following file sinks:
<ul>
<li>3GP file sink</li>
<li>MP3 file sink</li>
<li>MP4 file sink</li>
</ul>The transcode sink activation object exposes the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a> interface.

## -parameters

### -param ppActivate [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface. This interface is used to create the file sink instance from the activation object. Before doing so, query the returned pointer for the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a> interface and use that interface to initialize the object.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftranscodesinkinfoprovider">IMFTranscodeSinkInfoProvider</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>