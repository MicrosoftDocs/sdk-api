---
UID: NN:d2d1_1.ID2D1Bitmap1
title: ID2D1Bitmap1
author: windows-sdk-content
description: Represents a bitmap that can be used as a surface for an ID2D1DeviceContext or mapped into system memory, and can contain additional color context information.
old-location: direct2d\id2d1bitmap1.htm
tech.root: direct2d
ms.assetid: 669a9377-248c-4a86-b447-ed117fff43a6
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: ID2D1Bitmap1, ID2D1Bitmap1 interface [Direct2D], ID2D1Bitmap1 interface [Direct2D],described, d2d1_1/ID2D1Bitmap1, direct2d.id2d1bitmap1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Bitmap1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Bitmap1 interface


## -description


Represents a bitmap that can be used as a surface for an <a href="https://msdn.microsoft.com/a54dd628-c2a2-4b04-9ced-7749a395f187">ID2D1DeviceContext</a> or mapped into system memory, and can contain additional color context information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1Bitmap1</b> interface inherits from <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>. <b>ID2D1Bitmap1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1Bitmap1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ab8bed5-c124-4e14-8a05-3a71f07f5fd1">GetColorContext</a>
</td>
<td align="left" width="63%">
Gets the color context information associated with the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63e13172-7c6a-49af-aef9-83bf12a1f7d5">GetOptions</a>
</td>
<td align="left" width="63%">
Gets the options used in creating the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82d41172-bc24-48eb-ae0e-60947751eec6">GetSourceStream</a>
</td>
<td align="left" width="63%">
Gets any image stream that is associated with the bitmap.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f9cb3830-7c1a-4254-a3fd-f1c056bec0c0">GetSurface</a>
</td>
<td align="left" width="63%">
Gets either the surface that was specified when the bitmap was created, or the default surface created when the bitmap was created. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/284c16ea-1a9f-4f13-b359-214178650add">Map</a>
</td>
<td align="left" width="63%">
Maps  the given bitmap into memory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/471c6e8a-4412-4efc-a7bf-688b1da7e367">Unmap</a>
</td>
<td align="left" width="63%">
Unmaps the bitmap from memory. 

</td>
</tr>
</table> 


## -remarks



<h3><a id="Creating_ID2D1Bitmap_Objects"></a><a id="creating_id2d1bitmap_objects"></a><a id="CREATING_ID2D1BITMAP_OBJECTS"></a>Creating ID2D1Bitmap Objects</h3>
Use one of these methods to create an <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> object. <ul>
<li>
<a href="https://msdn.microsoft.com/8292da6b-8232-4ef0-967d-a53d586aa9a9">ID2D1DeviceContext::CreateBitmap</a>
</li>
<li>
<a href="https://msdn.microsoft.com/98BA78CD-4902-43B9-A412-895CA2A112C7">ID2D1DeviceContext::CreateBitmapFromWicBitmap</a>
</li>
</ul>


For information about the pixel formats supported by Direct2D bitmaps, see <a href="https://msdn.microsoft.com/09b1f9c6-1780-4733-ac22-9e8c21466b67">Supported Pixel Formats and Alpha Modes</a>.

An <a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a> is a device-dependent resource: your application should create bitmaps after it initializes the render target with which the bitmap will be used, and recreate the bitmap whenever the render target needs recreated. (For more information about resources, see <a href="https://msdn.microsoft.com/afd308a7-9524-4436-9a0e-8575383d96fa">Resources Overview</a>.)




## -see-also




<a href="https://msdn.microsoft.com/e58216ea-e6b5-450f-a0ea-b879aa5dff38">ID2D1Bitmap</a>
 

 

