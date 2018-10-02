---
UID: NF:oleidl.IOleInPlaceFrame.InsertMenus
title: IOleInPlaceFrame::InsertMenus
author: windows-sdk-content
description: Enables the container to insert menu groups into the composite menu to be used during the in-place session.
old-location: com\ioleinplaceframe_insertmenus.htm
tech.root: com
ms.assetid: 659ea109-c2c1-4146-aed2-60b1ce853d89
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IOleInPlaceFrame interface [COM],InsertMenus method, IOleInPlaceFrame.InsertMenus, IOleInPlaceFrame::InsertMenus, InsertMenus, InsertMenus method [COM], InsertMenus method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_insertmenus, com.ioleinplaceframe_insertmenus, oleidl/IOleInPlaceFrame::InsertMenus
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
 - IOleInPlaceFrame.InsertMenus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleInPlaceFrame::InsertMenus


## -description


Enables the container to insert menu groups into the composite menu to be used during the in-place session.


## -parameters




### -param hmenuShared [in]

A handle to an empty menu.


### -param lpMenuWidths [in, out]

A pointer to an <a href="https://msdn.microsoft.com/e6ad4ab7-0e53-4fad-8f2e-a0ff7b376815">OLEMENUGROUPWIDTHS</a> array with six elements. The container fills in elements 0, 2, and 4 to reflect the number of menu elements it provided in the <b>File</b>, <b>View</b>, and <b>Window</b> menu groups.


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
This method is called by object applications when they are first being activated. They call it to insert their menus into the frame-level user interface.

The object application asks the container to add its menus to the menu specified in <i>hmenuShared</i> and to set the group counts in the <a href="https://msdn.microsoft.com/e6ad4ab7-0e53-4fad-8f2e-a0ff7b376815">OLEMENUGROUPWIDTHS</a> array pointed to by <i>lpMenuWidths</i>. The object application then adds its own menus and counts. Objects can call <b>IOleInPlaceFrame::InsertMenus</b> as many times as necessary to build up the composite menus. The container should use the initial menu handle associated with the composite menu for all menu items in the drop-down menus.




## -see-also




<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>
 

 

