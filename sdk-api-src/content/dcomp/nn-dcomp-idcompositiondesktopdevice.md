---
UID: NN:dcomp.IDCompositionDesktopDevice
title: IDCompositionDesktopDevice (dcomp.h)
author: windows-sdk-content
description: An application must use the IDCompositionDesktopDevice interface in order to use DirectComposition in a Win32 desktop application.
old-location: directcomp\idcompositiondesktopdevice.htm
tech.root: directcomp
ms.assetid: 0FCDCDC2-541A-4EB5-A7FF-492AB5C25F7B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionDesktopDevice, IDCompositionDesktopDevice interface [DirectComposition], IDCompositionDesktopDevice interface [DirectComposition],described, dcomp/IDCompositionDesktopDevice, directcomp.idcompositiondesktopdevice
ms.topic: interface
f1_keywords: 
 - "dcomp/IDCompositionDesktopDevice"
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDesktopDevice
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDesktopDevice interface


## -description


An application must use the IDCompositionDesktopDevice interface in order to use DirectComposition in a Win32 desktop application. This interface allows the application to connect a visual tree to a window and to host layered child windows for composition


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDCompositionDesktopDevice</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>. <b>IDCompositionDesktopDevice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDCompositionDesktopDevice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondesktopdevice-createsurfacefromhandle">CreateSurfaceFromHandle</a>
</td>
<td align="left" width="63%">
Creates a new composition surface object that wraps an existing composition surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondesktopdevice-createsurfacefromhwnd">CreateSurfaceFromHwnd</a>
</td>
<td align="left" width="63%">
Creates a wrapper object that represents the rasterization of a layered window, and that can be associated with a visual for composition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositiondesktopdevice-createtargetforhwnd">CreateTargetForHwnd</a>
</td>
<td align="left" width="63%">
Creates a composition target object that is bound to the window that is represented by the specified window handle.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>
 

 

