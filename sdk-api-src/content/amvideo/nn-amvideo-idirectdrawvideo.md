---
UID: NN:amvideo.IDirectDrawVideo
title: IDirectDrawVideo
author: windows-driver-content
description: The IDirectDrawVideo interface queries the Video Renderer filter about DirectDraw surfaces and hardware capabilities.Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of.
old-location: dshow\idirectdrawvideo.htm
old-project: DirectShow
ms.assetid: b918bf3b-b91b-40fb-abb8-4115a4f254bb
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDirectDrawVideo, IDirectDrawVideo interface [DirectShow], IDirectDrawVideo interface [DirectShow], described, IDirectDrawVideoInterface, amvideo/IDirectDrawVideo, dshow.idirectdrawvideo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDirectDrawVideo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IDirectDrawVideo interface


## -description



The <code>IDirectDrawVideo</code> interface queries the <a href="https://msdn.microsoft.com/7719ed9d-e3b9-4c84-b587-4e120b5cabf8">Video Renderer</a> filter about DirectDraw surfaces and hardware capabilities.

Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of. For example, if you are positive that you don't want the Video Renderer to use a hardware overlay you can disable its use via the <a href="https://msdn.microsoft.com/e6839757-2b63-497d-9978-35c8dfabc0ed">SetSwitches</a> method.

<div class="alert"><b>Note</b>  You can't use this interface to force the Video Renderer to use a particular DirectDraw feature; you can only stop it from using that feature.</div>
<div> </div>
There is some duplication in this interface with the <b>IDirectDraw</b> interface; however, this interface enables simple access to that information without calling the DirectDraw provider directly.

The Video Renderer does not load DirectDraw until it is connected, and likewise DirectDraw is unloaded only when the renderer is disconnected. When the renderer has allocated the DirectDraw surfaces it will use for video playback, an application can obtain a <b>DDSURFACEDESC</b> structure describing it. By passing in a pointer to a <b>DDSURFACEDESC</b> structure, the renderer will fill in the structure with the details of the current surface. If DirectDraw has not been loaded, the renderer will return E_FAIL. If the renderer is using DCI (the predecessor to DirectDraw), the <b>DDSURFACEDESC</b> structure is not filled in but the call will return S_FALSE. The only type of DCI surfaces the renderer uses are primary surfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawVideo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawVideo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawVideo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35af80c9-7cc7-46c7-899c-c47f56a4ec17">CanUseOverlayStretch</a>
</td>
<td align="left" width="63%">
Determines whether the renderer will check overlay restrictions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fa11ebb-0408-4ea7-9d18-c85860d6e2fc">CanUseScanLine</a>
</td>
<td align="left" width="63%">
Determines whether the renderer will check the current scan line when drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d63437e3-4e8a-49de-b555-db29d235569d">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves a DirectDraw-defined DDCAPS structure containing the hardware capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25c64d6e-fd49-430a-9f9b-3c2b3d43d3a1">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IDirectDraw</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/623cd000-6194-458d-8ef1-5eca202756c1">GetEmulatedCaps</a>
</td>
<td align="left" width="63%">
Retrieves a DirectDraw-defined DDCAPS structure containing the emulated capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3ea1c5c4-bf2e-40f6-bf48-a69900128ec8">GetFourCCCodes</a>
</td>
<td align="left" width="63%">
Retrieves the multimedia format type <b>FOURCC DWORD</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3884dbf-c75c-45f7-953c-bfdc14734820">GetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the DirectDraw surface in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5d5c608-1890-43f8-bdf3-3fcb0c6a2f5e">GetSurfaceType</a>
</td>
<td align="left" width="63%">
Retrieves the actual surface type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a9e3c46-6d2d-474e-ab72-f67b5ed450f2">GetSwitches</a>
</td>
<td align="left" width="63%">
Retrieves the surface types that the renderer is allowed to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9525ee57-3c53-42db-bc40-eb1d4658d9b6">SetDefault</a>
</td>
<td align="left" width="63%">
Makes the current property settings the global default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd7b9571-2edb-4f36-b7a3-b280c37cb471">SetDirectDraw</a>
</td>
<td align="left" width="63%">
Passes the <b>IDirectDraw</b> interface to a loaded driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6839757-2b63-497d-9978-35c8dfabc0ed">SetSwitches</a>
</td>
<td align="left" width="63%">
Sets the surface types that the renderer is allowed to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e617b40d-ba5b-4fc8-825e-3c751f72bc2c">UseOverlayStretch</a>
</td>
<td align="left" width="63%">
Determines whether the renderer should check overlay stretch limitations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8378582d-ef82-47ff-a801-934c900ac328">UseScanLine</a>
</td>
<td align="left" width="63%">
Determines whether the renderer should check the current scan line when drawing a video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e50f7f06-6534-4373-a2b8-fa315158729d">UseWhenFullScreen</a>
</td>
<td align="left" width="63%">
Determines whether DirectShow should change display mode when going to full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de2addfc-e289-4277-a283-b7aa2aa47ba0">WillUseFullScreen</a>
</td>
<td align="left" width="63%">
Determines whether DirectShow will change display mode when going to full-screen mode.

</td>
</tr>
</table> 

