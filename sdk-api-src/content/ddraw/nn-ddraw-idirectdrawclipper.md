---
UID: NN:ddraw.IDirectDrawClipper
title: IDirectDrawClipper (ddraw.h)

description: Applications use the methods of the IDirectDrawClipper interface to manage clip lists. This section is a reference to the methods of this interface.
old-location: directdraw\idirectdrawclipper.htm
tech.root: directdraw
ms.assetid: 2e93583a-59a8-4a0f-9299-ed57fdcebf33

ms.date: 12/05/2018
ms.keywords: IDirectDrawClipper, IDirectDrawClipper interface [DirectDraw], IDirectDrawClipper interface [DirectDraw],described, ddraw/IDirectDrawClipper, directdraw.idirectdrawclipper
ms.topic: interface
f1_keywords: 
 - "ddraw/IDirectDrawClipper"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawClipper interface


## -description


Applications use the methods of the <b>IDirectDrawClipper</b> interface to manage clip lists. This section is a reference to the methods of this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawClipper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawClipper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-getcliplist">GetClipList</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the clip list that is associated with a DirectDrawClipper object. To select a subset of the clip list, you can pass a rectangle that clips the clip list.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-gethwnd">GetHWnd</a>
</td>
<td align="left" width="63%">
Retrieves the window handle that was previously associated with this DirectDrawClipper object by the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">IDirectDrawClipper::SetHWnd</a> method.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes a DirectDrawClipper object that was created by using the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> COM function.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-iscliplistchanged">IsClipListChanged</a>
</td>
<td align="left" width="63%">
Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-setcliplist">SetClipList</a>
</td>
<td align="left" width="63%">
Sets or deletes the clip list that is used by the <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-blt">IDirectDrawSurface7::Blt</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-bltbatch">IDirectDrawSurface7::BltBatch</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay">IDirectDrawSurface7::UpdateOverlay</a> methods on surfaces to which the parent DirectDrawClipper object is attached.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">SetHWnd</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-initialize">Initialize</a>
</td>
</tr>
<tr>
<td>Clip list</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-getcliplist">GetClipList</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-iscliplistchanged">IsClipListChanged</a>, <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-setcliplist">SetClipList</a>,  and <a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-sethwnd">SetHWnd</a>
</td>
</tr>
<tr>
<td>Handles</td>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nf-ddraw-idirectdrawclipper-gethwnd">GetHWnd</a>
</td>
</tr>
</table>
 



You can use the LPDIRECTDRAWCLIPPER data type to declare a variable that contains a pointer to an <b>IDirectDrawClipper</b> interface. The Ddraw.h header file declares this data type with the following code:




```

typedef struct IDirectDrawClipper    FAR *LPDIRECTDRAWCLIPPER;

```




