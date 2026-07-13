---
UID: NN:wiavideo.IWiaVideo
title: IWiaVideo (wiavideo.h)
description: The IWiaVideo interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.Note  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use DirectShow to acquire images from video.
helpviewer_keywords: ["IWiaVideo","IWiaVideo interface [WIA]","IWiaVideo interface [WIA]","described","_wia_IWiaVideo","wia._wia_IWiaVideo","wiavideo/IWiaVideo"]
old-location: wia\_wia_IWiaVideo.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiavideo\iwiavideo.htm
ms.date: 12/05/2018
ms.keywords: IWiaVideo, IWiaVideo interface [WIA], IWiaVideo interface [WIA],described, _wia_IWiaVideo, wia._wia_IWiaVideo, wiavideo/IWiaVideo
req.header: wiavideo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wiavideo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaVideo
 - wiavideo/IWiaVideo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiavideo.dll
api_name:
 - IWiaVideo
archived: true
---

# IWiaVideo interface


## -description

The <b>IWiaVideo</b> interface provides methods that allow an application that uses Windows Image Acquisition (WIA) services to acquire still images from a streaming video device.


<div class="alert"><b>Note</b>  WIA does not support video devices in Windows Server 2003, Windows Vista, and later. For those versions of the Windows, use <a href="/previous-versions/ms783323(v=vs.85)">DirectShow</a> to acquire images from video.</div><div> </div>

## -inheritance

The <b>IWiaVideo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWiaVideo</b> also has these types of members:

## -remarks

The <b>IWiaVideo</b> interface, like all Component Object Model (COM) interfaces, inherits the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface methods. 

<table class="clsStd">
<tr>
<th>IUnknown Methods</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>
</td>
<td>Returns pointers to supported interfaces.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">IUnknown::AddRef</a>
</td>
<td>Increments reference count.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a>
</td>
<td>Decrements reference count.</td>
</tr>
</table>
