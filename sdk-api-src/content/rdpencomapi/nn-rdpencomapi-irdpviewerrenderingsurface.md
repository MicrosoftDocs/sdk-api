---
UID: NN:rdpencomapi.IRDPViewerRenderingSurface
title: IRDPViewerRenderingSurface (rdpencomapi.h)
description: Manages the rendering surface for the viewer.
helpviewer_keywords: ["IRDPViewerRenderingSurface","IRDPViewerRenderingSurface interface [RDP]","IRDPViewerRenderingSurface interface [RDP]","described","rdp.irdpviewerrenderingsurface","rdpencomapi/IRDPViewerRenderingSurface"]
old-location: rdp\irdpviewerrenderingsurface.htm
tech.root: rdp
ms.assetid: 24d818ec-f58d-4bf1-adf8-c15560595147
ms.date: 12/05/2018
ms.keywords: IRDPViewerRenderingSurface, IRDPViewerRenderingSurface interface [RDP], IRDPViewerRenderingSurface interface [RDP],described, rdp.irdpviewerrenderingsurface, rdpencomapi/IRDPViewerRenderingSurface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPViewerRenderingSurface
 - rdpencomapi/IRDPViewerRenderingSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPViewerRenderingSurface
---

# IRDPViewerRenderingSurface interface


## -description

<p class="CCE_Message">[The <b>IRDPViewerRenderingSurface</b> interface is no longer available for use as of Windows 10, version 1709.]

Manages the rendering surface for the viewer. The viewer control host uses this interface to set the rendering surface that the viewer should use.

This interface is implemented by the viewer control. An instance of this interface is obtained by calling the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiviewer">IRDPSRAPIViewer</a> object's <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method, passing <b>IID_IRDPViewerRenderingSurface</b>.

## -inheritance

The <b>IRDPViewerRenderingSurface</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRDPViewerRenderingSurface</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -members

The <b>IRDPViewerRenderingSurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpviewerrenderingsurface-setrenderingsurface">SetRenderingSurface</a>
</td>
<td align="left" width="63%">
Sets the rendering surface to be used by the viewer.

</td>
</tr>
</table>