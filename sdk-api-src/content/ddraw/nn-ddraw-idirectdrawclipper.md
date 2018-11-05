---
UID: NN:ddraw.IDirectDrawClipper
title: IDirectDrawClipper
author: windows-sdk-content
description: Applications use the methods of the IDirectDrawClipper interface to manage clip lists. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawclipper.htm
tech.root: directdraw
ms.assetid: 2e93583a-59a8-4a0f-9299-ed57fdcebf33
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirectDrawClipper, IDirectDrawClipper interface [DirectDraw], IDirectDrawClipper interface [DirectDraw],described, ddraw/IDirectDrawClipper, directdraw.idirectdrawclipper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawClipper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawClipper interface


## -description


Applications use the methods of the <b>IDirectDrawClipper</b> interface to manage clip lists. This section is a reference to the methods of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawClipper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDirectDrawClipper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawClipper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0446f8b9-c965-4336-ae78-5bb791861844">GetClipList</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the clip list that is associated with a DirectDrawClipper object. To select a subset of the clip list, you can pass a rectangle that clips the clip list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/025e898f-e160-4485-87cf-f5fbc014e9f1">GetHWnd</a>
</td>
<td align="left" width="63%">
Retrieves the window handle that was previously associated with this DirectDrawClipper object by the <a href="https://msdn.microsoft.com/7683bccd-3f5c-4098-9041-9c66853cda0e">IDirectDrawClipper::SetHWnd</a> method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0b71af4-f806-4264-bd14-b556b31aab29">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDrawClipper object that was created by using the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> COM function.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d394b638-6015-47d8-89ea-2ed71611ddb3">IsClipListChanged</a>
</td>
<td align="left" width="63%">
Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/717f51e0-80cb-4762-b05d-30e30d065d0c">SetClipList</a>
</td>
<td align="left" width="63%">
Sets or deletes the clip list that is used by the <a href="https://msdn.microsoft.com/e458c430-855c-419b-aa50-144d2b422e78">IDirectDrawSurface7::Blt</a>, <a href="https://msdn.microsoft.com/50c071a6-2963-474e-994e-c789b1924d92">IDirectDrawSurface7::BltBatch</a>, and <a href="https://msdn.microsoft.com/8706c6ca-cd17-490a-8ff9-9470a7d7a150">IDirectDrawSurface7::UpdateOverlay</a> methods on surfaces to which the parent DirectDrawClipper object is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7683bccd-3f5c-4098-9041-9c66853cda0e">SetHWnd</a>
</td>
<td align="left" width="63%">
Sets the window handle that the clipper object uses to obtain clipping information.

</td>
</tr>
</table> 


## -remarks



The methods of the <b>IDirectDrawClipper</b> interface can be organized into the following groups:<table>
<tr>
<th>Group</th>
<th>Methods</th>
</tr>
<tr>
<td>Allocating memory</td>
<td>
<a href="https://msdn.microsoft.com/b0b71af4-f806-4264-bd14-b556b31aab29">Initialize</a>
</td>
</tr>
<tr>
<td>Clip list</td>
<td>
<a href="https://msdn.microsoft.com/0446f8b9-c965-4336-ae78-5bb791861844">GetClipList</a>, <a href="https://msdn.microsoft.com/d394b638-6015-47d8-89ea-2ed71611ddb3">IsClipListChanged</a>, <a href="https://msdn.microsoft.com/717f51e0-80cb-4762-b05d-30e30d065d0c">SetClipList</a>,  and <a href="https://msdn.microsoft.com/7683bccd-3f5c-4098-9041-9c66853cda0e">SetHWnd</a>
</td>
</tr>
<tr>
<td>Handles</td>
<td>
<a href="https://msdn.microsoft.com/025e898f-e160-4485-87cf-f5fbc014e9f1">GetHWnd</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWCLIPPER data type to declare a variable that contains a pointer to an <b>IDirectDrawClipper</b> interface. The Ddraw.h header file declares this data type with the following code:



<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
typedef struct IDirectDrawClipper    FAR *LPDIRECTDRAWCLIPPER;
</pre>
</td>
</tr>
</table></span></div>


