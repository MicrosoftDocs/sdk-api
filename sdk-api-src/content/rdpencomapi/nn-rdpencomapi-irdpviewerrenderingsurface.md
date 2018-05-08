---
UID: NN:rdpencomapi.IRDPViewerRenderingSurface
title: IRDPViewerRenderingSurface
author: windows-driver-content
description: Manages the rendering surface for the viewer.
old-location: rdp\irdpviewerrenderingsurface.htm
old-project: Rdp
ms.assetid: 24d818ec-f58d-4bf1-adf8-c15560595147
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPViewerRenderingSurface, IRDPViewerRenderingSurface interface [RDP], IRDPViewerRenderingSurface interface [RDP],described, rdp.irdpviewerrenderingsurface, rdpencomapi/IRDPViewerRenderingSurface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPViewerRenderingSurface
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRDPViewerRenderingSurface interface


## -description


<p class="CCE_Message">[The <b>IRDPViewerRenderingSurface</b> interface is no longer available for use as of Windows 10, version 1709.]

Manages the rendering surface for the viewer. The viewer control host uses this interface to set the rendering surface that the viewer should use.

This interface is implemented by the viewer control. An instance of this interface is obtained by calling the <a href="https://msdn.microsoft.com/6bafe380-2ef4-4e93-a6cd-143798437615">IRDPSRAPIViewer</a> object's <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method, passing <b>IID_IRDPViewerRenderingSurface</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPViewerRenderingSurface</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPViewerRenderingSurface</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPViewerRenderingSurface</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e70541ab-fc23-4960-be38-8eb6849ab14f">SetRenderingSurface</a>
</td>
<td align="left" width="63%">
Sets the rendering surface to be used by the viewer.

</td>
</tr>
</table> 

