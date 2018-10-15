---
UID: NN:shobjidl_core.IDragSourceHelper
title: IDragSourceHelper
author: windows-sdk-content
description: Exposed by the Shell to allow an application to specify the image that will be displayed during a Shell drag-and-drop operation.
old-location: shell\IDragSourceHelper.htm
tech.root: shell
ms.assetid: d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDragSourceHelper, IDragSourceHelper interface [Windows Shell], IDragSourceHelper interface [Windows Shell],described, _win32_IDragSourceHelper, shell.IDragSourceHelper, shobjidl_core/IDragSourceHelper
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDragSourceHelper
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDragSourceHelper interface


## -description


Exposed by the Shell to allow an application to specify the image that will be displayed during a Shell drag-and-drop operation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDragSourceHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDragSourceHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDragSourceHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d50be9c9-f407-4386-bb8f-04c849205359">InitializeFromBitmap</a>
</td>
<td align="left" width="63%">
Initializes the drag-image manager for a windowless control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0bcdfe92-cec0-44f3-a345-5b560d52fae9">InitializeFromWindow</a>
</td>
<td align="left" width="63%">
Initializes the drag-image manager for a control with a window.

</td>
</tr>
</table> 


## -remarks



This interface is exposed by the Shell's drag-image manager. It is not implemented by applications.

Use this interface to specify the image displayed during a Shell drag-and-drop operation. The <b>IDragSourceHelper</b>,  <a href="https://msdn.microsoft.com/b1ddbf7e-edf3-48fb-8983-ae39cb7bb4b0">IDropTargetHelper</a>, and <a href="https://msdn.microsoft.com/8421BFA0-0655-447c-99BB-3D4F049C572D">IInitializeWithWindow</a> interfaces are exposed by the drag-image manager object to allow the <a href="https://msdn.microsoft.com/13fbe834-1ef8-4944-b2e4-9f5c413c65c8">IDropTarget</a> interface to use custom drag images. To use either of these interfaces, you must create an in-process server drag-image manager object by calling <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> with a class identifier (CLSID) of CLSID_DragDropHelper. Get interface pointers using standard Component Object Model (COM) procedures.

The <b>IDragSourceHelper</b> interface provides the following two ways to specify the bitmap to be used as a drag image.

				

<ul>
<li>Controls that have a window can register a DI_GETDRAGIMAGE window message for it and initialize the drag-image manager with <a href="https://msdn.microsoft.com/0bcdfe92-cec0-44f3-a345-5b560d52fae9">IDragSourceHelper::InitializeFromWindow</a>. When the DI_GETDRAGIMAGE message is received, the handler puts the drag image bitmap information in the <a href="https://msdn.microsoft.com/e0dd76b2-fd5c-41e8-b540-db90a2f0dcec">SHDRAGIMAGE</a> structure that is passed as the message's <i>lParam</i> value.</li>
<li>Windowless controls can initialize the drag-image manager with <a href="https://msdn.microsoft.com/d50be9c9-f407-4386-bb8f-04c849205359">IDragSourceHelper::InitializeFromBitmap</a>. This method allows an application to simply specify the bitmap.</li>
</ul>
<div class="alert"><b>Note</b>   The drag-and-drop helper object calls <a href="https://msdn.microsoft.com/7430d12c-ab07-4a9c-a845-4743818afbc7">IDataObject::SetData</a> to load private formats—used for cross-process support—into the data object. It later retrieves these formats by calling <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. To support the drag-and-drop helper object, the data object's <b>SetData</b> and <b>GetData</b> implementations must be able to accept and return arbitrary private formats.</div>
<div> </div>
For further discussion of Shell drag-and-drop operations, see <a href="https://msdn.microsoft.com/bd73098b-2f69-48a4-bb06-e1e0a452e69d">Transferring Shell Data Using Drag-and-Drop or the Clipboard</a>.

<div class="alert"><b>Note</b>   Prior to Windows Vista this interface was declared in Shlobj.h.</div>
<div> </div>


