---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# SHDoDragDrop function


## -description


Executes a drag-and-drop operation. Supports drag source creation on demand, as well as drag images.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window used to obtain the drag image. This value can be <b>NULL</b>. See Remarks for more details.


### -param pdata

TBD


### -param pdsrc [in]

Type: <b><a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a>*</b>

A pointer to an implementation of the <a href="https://msdn.microsoft.com/963a36bc-4ad7-4591-bffc-a96b4310177d">IDropSource</a> interface, which is used to communicate with the source during the drag operation.
        
                        

As of Windows Vista, if this value is <b>NULL</b>, the Shell creates a drop source object for you.


### -param dwEffect [in]

Type: <b>DWORD</b>

The effects that the source allows in the drag-and-drop operation. The most significant effect is whether the drag-and-drop operation permits a move. For a list of possible values, see <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a>.


### -param pdwEffect [out]

Type: <b>DWORD*</b>

A pointer to a value that indicates how the drag-and-drop operation affected the source data. The <i>pdwEffect</i> parameter is set only if the operation is not canceled. For a list of possible values, see <a href="https://msdn.microsoft.com/d8e46899-3fbf-4012-8dd3-67fa627526d5">DROPEFFECT</a>.


#### - pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on a data object that contains the data being dragged.


## -returns



Type: <b>HRESULT</b>

This function supports the standard return value E_OUTOFMEMORY, as well as the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_DROP</b></dt>
</dl>
</td>
<td width="60%">
The drag-and-drop operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The drag-and-drop operation was canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSPEC</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
</table>
 




## -remarks



As of Windows Vista, if a drag image is not already stored in the data object <i>pdtobj</i> and a drag image cannot be obtained from the window specified by <i>hwnd</i>, the Shell provides a generic drag image. A drag image can fail to be obtained from the specified window either because <i>hwnd</i> is <b>NULL</b> or the specified window does not support the DI_GETDRAGIMAGE message.



