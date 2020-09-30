---
UID: NN:strmif.IVPManager
title: IVPManager (strmif.h)
description: The IVPManager interface is implemented on the Video Port Manager (VPM).
helpviewer_keywords: ["IVPManager","IVPManager interface [DirectShow]","IVPManager interface [DirectShow]","described","IVPManagerInterface","dshow.ivpmanager","strmif/IVPManager"]
old-location: dshow\ivpmanager.htm
tech.root: dshow
ms.assetid: 9064daa7-5868-49a5-9fd6-9a332ab3b470
ms.date: 12/05/2018
ms.keywords: IVPManager, IVPManager interface [DirectShow], IVPManager interface [DirectShow],described, IVPManagerInterface, dshow.ivpmanager, strmif/IVPManager
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVPManager
 - strmif/IVPManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVPManager
---

# IVPManager interface


## -description

The <code>IVPManager</code> interface is implemented on the <a href="/windows/desktop/DirectShow/video-port-manager">Video Port Manager</a> (VPM). The interface provides methods for applications to specify and retrieve indexes for ports when there are multiple video ports on a system, and to specify and retrieve the rectangle used by the video port. Currently, only the two index-related methods are implemented.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVPManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/strmif/nf-strmif-ivpmanager-getvideoportindex">GetVideoPortIndex</a>
</td>
<td align="left" width="63%">
Returns the current video port index being used by the Video Port Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/strmif/nf-strmif-ivpmanager-setvideoportindex">SetVideoPortIndex</a>
</td>
<td align="left" width="63%">
Instructs the Video Port Manager to connect to the specified video port.

</td>
</tr>
</table>