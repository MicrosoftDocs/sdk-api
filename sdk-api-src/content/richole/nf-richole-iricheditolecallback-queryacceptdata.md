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

# IRichEditOleCallback::QueryAcceptData


## -description


During a paste operation or a drag event, determines if the data that is pasted or dragged should be accepted.


## -parameters




### -param lpdataobj

Type: <b>LPDATAOBJECT</b>

The data object being pasted or dragged. 


### -param lpcfFormat

Type: <b>CLIPFORMAT*</b>

The clipboard format that will be used for the paste or drop operation. If the value pointed to by 
					<i>lpcfFormat</i> is zero, the best available format will be used. If the callback changes the value pointed to by 
					<i>lpcfFormat</i>, the rich edit control only uses that format and the operation will fail if the format is not available. 


### -param reco

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A clipboard operation flag, which can be one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RECO_DROP"></a><a id="reco_drop"></a><dl>
<dt><b>RECO_DROP</b></dt>
</dl>
</td>
<td width="60%">
Drop operation (drag-and-drop).

</td>
</tr>
<tr>
<td width="40%"><a id="RECO_PASTE"></a><a id="reco_paste"></a><dl>
<dt><b>RECO_PASTE</b></dt>
</dl>
</td>
<td width="60%">
Paste from the clipboard.

</td>
</tr>
</table>
 


### -param fReally

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Indicates whether the drag-drop is actually happening or if it is just a query. A nonzero value indicates the paste or drop is actually happening. A zero value indicates the operation is just a query, such as for 
					<a href="https://msdn.microsoft.com/1b858ad8-1312-407b-b12a-c63668ba9f72">EM_CANPASTE</a>.


### -param hMetaPict

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HGLOBAL</a></b>

Handle to a metafile containing the icon view of an object if <b>DVASPECT_ICON</b> is being imposed on an object by a paste special operation. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns <b>S_OK</b> on success. See Remarks.




## -remarks



 On failure, the rich edit control refuses the data and terminates the operation. Otherwise, the control checks the data itself for acceptable formats. A success code other than <b>S_OK</b> means that the callback either checked the data itself (if <i>fReally</i> is <b>FALSE</b>) or imported the data itself (if <i>fReally</i> is <b>TRUE</b>). If the application returns a success code other than <b>S_OK</b>, the control does not check the read-only state of the edit control.
	




## -see-also




<a href="https://msdn.microsoft.com/2c3ba341-f62f-4c95-9547-6d50fcf3d6b4">IRichEditOleCallback</a>
 

 

