---
UID: NF:oleidl.IOleInPlaceFrame.SetMenu
title: IOleInPlaceFrame::SetMenu
author: windows-sdk-content
description: Adds a composite menu to the window frame containing the object being activated in place.
old-location: com\ioleinplaceframe_setmenu.htm
tech.root: com
ms.assetid: dc26a399-846d-4d15-b406-752350e528c2
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IOleInPlaceFrame interface [COM],SetMenu method, IOleInPlaceFrame.SetMenu, IOleInPlaceFrame::SetMenu, SetMenu, SetMenu method [COM], SetMenu method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_setmenu, com.ioleinplaceframe_setmenu, oleidl/IOleInPlaceFrame::SetMenu
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
 - IOleInPlaceFrame.SetMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceFrame::SetMenu


## -description


Adds a composite menu to the window frame containing the object being activated in place.


## -parameters




### -param hmenuShared [in]

A handle to the composite menu constructed by calls to <a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a> and the <a href="_win32_InsertMenu_cpp">InsertMenu</a> function.


### -param holemenu [in]

A handle to the menu descriptor returned by the <a href="https://msdn.microsoft.com/b4a6b3f1-aee9-4b68-8ffe-24bd497db0a0">OleCreateMenuDescriptor</a> function.


### -param hwndActiveObject [in]

A handle to a window owned by the object and to which menu messages, commands, and accelerators are to be sent.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The object calls <b>IOleInPlaceFrame::SetMenu</b> to ask the container to install the composite menu structure set up by calls to <a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
An SDI container's implementation of this method should call the <a href="_win32_SetMenu_cpp">SetMenu</a> function. An MDI container should send a <a href="_win32_WM_MDISETMENU_cpp">WM_MDISETMENU</a> message, using <i>hmenuShared</i> as the menu to install. The container should call <a href="https://msdn.microsoft.com/c80fe36d-5093-4814-83a9-0c11c5a7cf5f">OleSetMenuDescriptor</a> to install the OLE dispatching code.

When deactivating, the container must call <b>IOleInPlaceFrame::SetMenu</b>, specifying <b>NULL</b> to remove the shared menu. This is done to help minimize window repaints. The container should also call <a href="https://msdn.microsoft.com/c80fe36d-5093-4814-83a9-0c11c5a7cf5f">OleSetMenuDescriptor</a>, specifying <b>NULL</b> to unhook the dispatching code. Finally, the object application calls <a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a> to free the data structure.

<div class="alert"><b>Note</b>  While executing <b>IOleInPlaceFrame::SetMenu</b>, do not make calls to the <a href="_win32_PeekMessage_cpp">PeekMessage</a> or <a href="_win32_GetMessage_cpp">GetMessage</a> functions, or a dialog box. Doing so may cause the system to deadlock. There are further restrictions on which OLE interface methods and functions can be called from within <b>IOleInPlaceFrame::SetMenu</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>



<a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a>



<a href="_win32_InsertMenu_cpp">InsertMenu</a>



<a href="https://msdn.microsoft.com/dc347d39-a7bb-4bbf-8957-c3fbcff461bf">OleDestroyMenuDescriptor</a>



<a href="https://msdn.microsoft.com/c80fe36d-5093-4814-83a9-0c11c5a7cf5f">OleSetMenuDescriptor</a>
 

 

