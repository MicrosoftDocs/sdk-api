---
UID: NF:oleidl.IOleInPlaceUIWindow.SetBorderSpace
title: IOleInPlaceUIWindow::SetBorderSpace
author: windows-sdk-content
description: Allocates space for the border requested in the call to IOleInPlaceUIWindow::RequestBorderSpace.
old-location: com\ioleinplaceuiwindow_setborderspace.htm
tech.root: com
ms.assetid: 7c806a02-db6d-444e-a049-22c4ae2b19b0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOleInPlaceUIWindow interface [COM],SetBorderSpace method, IOleInPlaceUIWindow.SetBorderSpace, IOleInPlaceUIWindow::SetBorderSpace, SetBorderSpace, SetBorderSpace method [COM], SetBorderSpace method [COM],IOleInPlaceUIWindow interface, _ole_ioleinplaceuiwindow_setborderspace, com.ioleinplaceuiwindow_setborderspace, oleidl/IOleInPlaceUIWindow::SetBorderSpace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceUIWindow.SetBorderSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceUIWindow::SetBorderSpace


## -description


Allocates space for the border requested in the call to <a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">IOleInPlaceUIWindow::RequestBorderSpace</a>.


## -parameters




### -param pborderwidths [in]

Pointer to a <a href="_shell_BORDERWIDTHS_cpp">BORDERWIDTHS</a> structure containing the requested width of the tools, in pixels. It can be <b>NULL</b>, indicating the object does not need any space.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_INVALIDRECT</b></dt>
</dl>
</td>
<td width="60%">
The rectangle does not lie within the specifications returned by <a href="https://msdn.microsoft.com/9ee9970a-b937-4538-b3b8-460647086db1">IOleInPlaceUIWindow::GetBorder</a>.

</td>
</tr>
</table>
 




## -remarks



The object must call <b>IOleInPlaceUIWindow::SetBorderSpace</b>. It can do any one of the following:

<ul>
<li>Use its own toolbars, requesting border space of a specific size.</li>
<li>Use no toolbars, but force the container to remove its toolbars by passing a valid <a href="_shell_BORDERWIDTHS_cpp">BORDERWIDTHS</a> structure containing nothing but zeros in the <i>pborderwidths</i> parameter.</li>
<li>Use no toolbars but allow the in-place container to leave its toolbars up by passing <b>NULL</b> as the <i>pborderwidths</i> parameter.</li>
</ul>
The <a href="_shell_BORDERWIDTHS_cpp">BORDERWIDTHS</a> structure used in this call would generally have been passed in a previous call to <a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">IOleInPlaceUIWindow::RequestBorderSpace</a>, which must have returned S_OK.

If an object must renegotiate space on the border, it can call <b>IOleInPlaceUIWindow::SetBorderSpace</b> again with the new widths. If the call to <b>IOleInPlaceUIWindow::SetBorderSpace</b> fails, the object can do a full negotiation for border space with calls to <a href="https://msdn.microsoft.com/9ee9970a-b937-4538-b3b8-460647086db1">IOleInPlaceUIWindow::GetBorder</a>, <a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">IOleInPlaceUIWindow::RequestBorderSpace</a>, and <b>IOleInPlaceUIWindow::SetBorderSpace</b>.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceUIWindow::SetBorderSpace</b>, do not make calls to the <a href="_win32_PeekMessage_cpp">PeekMessage</a> or <a href="_win32_GetMessage_cpp">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceUIWindow::SetBorderSpace</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3cfb31aa-9746-438c-af64-8236c170fe88">IOleInPlaceUIWindow</a>



<a href="https://msdn.microsoft.com/9ee9970a-b937-4538-b3b8-460647086db1">IOleInPlaceUIWindow::GetBorder</a>



<a href="https://msdn.microsoft.com/fd477b1d-e9a5-4b99-adf1-8e62de975730">IOleInPlaceUIWindow::RequestBorderSpace</a>
 

 

