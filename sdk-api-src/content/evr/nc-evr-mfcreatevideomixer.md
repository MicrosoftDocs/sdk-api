---
UID: NC:evr.MFCreateVideoMixer
title: MFCreateVideoMixer (evr.h)
description: Creates the default video mixer for the enhanced video renderer (EVR).
helpviewer_keywords: ["MFCreateVideoMixer","MFCreateVideoMixer callback","MFCreateVideoMixer callback function [Media Foundation]","evr/MFCreateVideoMixer","fd817e1b-6f11-4cdc-aa21-e4ecda16bf1e","mf.mfcreatevideomixer"]
old-location: mf\mfcreatevideomixer.htm
tech.root: mfarchive
ms.assetid: fd817e1b-6f11-4cdc-aa21-e4ecda16bf1e
ms.date: 12/05/2018
ms.keywords: MFCreateVideoMixer, MFCreateVideoMixer callback, MFCreateVideoMixer callback function [Media Foundation], evr/MFCreateVideoMixer, fd817e1b-6f11-4cdc-aa21-e4ecda16bf1e, mf.mfcreatevideomixer
req.header: evr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateVideoMixer
 - evr/MFCreateVideoMixer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - evr.h
api_name:
 - MFCreateVideoMixer
---

## -description

Creates the default video mixer for the enhanced video renderer (EVR).

## -parameters

### -param pOwner

Pointer to the owner of this object. If the object is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.

### -param riidDevice

Interface identifier (IID) of the video device interface that will be used for processing the video. Currently the only supported value is IID_IDirect3DDevice9.

### -param riid

IID of the requested interface on the video mixer.  The video mixer exposes the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.

### -param ppv

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>