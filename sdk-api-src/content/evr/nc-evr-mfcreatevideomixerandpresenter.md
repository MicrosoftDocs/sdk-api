---
UID: NC:evr.MFCreateVideoMixerAndPresenter
title: MFCreateVideoMixerAndPresenter (evr.h)
description: Creates the default video mixer and video presenter for the enhanced video renderer (EVR).
helpviewer_keywords: ["1777027a-85bb-47d2-baf8-6f420282b01a","MFCreateVideoMixerAndPresenter","MFCreateVideoMixerAndPresenter callback","MFCreateVideoMixerAndPresenter callback function [Media Foundation]","evr/MFCreateVideoMixerAndPresenter","mf.mfcreatevideomixerandpresenter"]
old-location: mf\mfcreatevideomixerandpresenter.htm
tech.root: mf
ms.assetid: 1777027a-85bb-47d2-baf8-6f420282b01a
ms.date: 12/05/2018
ms.keywords: 1777027a-85bb-47d2-baf8-6f420282b01a, MFCreateVideoMixerAndPresenter, MFCreateVideoMixerAndPresenter callback, MFCreateVideoMixerAndPresenter callback function [Media Foundation], evr/MFCreateVideoMixerAndPresenter, mf.mfcreatevideomixerandpresenter
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
 - MFCreateVideoMixerAndPresenter
 - evr/MFCreateVideoMixerAndPresenter
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
 - MFCreateVideoMixerAndPresenter
archived: true
---

# MFCreateVideoMixerAndPresenter callback function


## -description

Creates the default video mixer and video presenter for the enhanced video renderer (EVR).

## -parameters

### -param pMixerOwner [in]

Pointer to the owner of the video mixer. If the mixer is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.

### -param pPresenterOwner [in]

Pointer to the owner of the video presenter. If the presenter is aggregated, pass a pointer to the aggregating object's <b>IUnknown</b> interface. Otherwise, set this parameter to <b>NULL</b>.

### -param riidMixer [in]

Interface identifier (IID) of the requested interface on the video mixer. The video mixer exposes the <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform">IMFTransform</a> interface.

### -param ppvVideoMixer [out]

Receives a pointer to the requested interface on the video mixer. The caller must release the interface.

### -param riidPresenter [in]

IID of the requested interface on the video presenter. The video presenter exposes the <a href="/windows/desktop/api/evr/nn-evr-imfvideopresenter">IMFVideoPresenter</a> interface.

### -param ppvVideoPresenter [out]

Receives a pointer to the requested interface on the video presenter. The caller must release the interface.

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
The method succeeded.
              

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>