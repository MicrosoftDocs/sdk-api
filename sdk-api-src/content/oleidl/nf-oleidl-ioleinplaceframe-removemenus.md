---
UID: NF:oleidl.IOleInPlaceFrame.RemoveMenus
title: IOleInPlaceFrame::RemoveMenus
author: windows-sdk-content
description: Removes a container's menu elements from the composite menu.
old-location: com\ioleinplaceframe_removemenus.htm
old-project: com
ms.assetid: 92d9fcda-8ede-4f38-ad56-59c4a75fe45a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOleInPlaceFrame interface [COM],RemoveMenus method, IOleInPlaceFrame.RemoveMenus, IOleInPlaceFrame::RemoveMenus, RemoveMenus, RemoveMenus method [COM], RemoveMenus method [COM],IOleInPlaceFrame interface, _ole_ioleinplaceframe_removemenus, com.ioleinplaceframe_removemenus, oleidl/IOleInPlaceFrame::RemoveMenus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleInPlaceFrame.RemoveMenus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOleInPlaceFrame::RemoveMenus


## -description


Removes a container's menu elements from the composite menu.


## -parameters




### -param hmenuShared [in]

A handle to the in-place composite menu that was constructed by calls to <a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a> and the <a href="https://msdn.microsoft.com/en-us/library/ms647987(v=VS.85).aspx">InsertMenu</a> function.


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



The object should always give the container a chance to remove its menu elements from the composite menu before deactivating the shared user interface.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
This method is called by the object application while it is being UI-deactivated to remove its menus.




## -see-also




<a href="https://msdn.microsoft.com/c530aff7-fd83-413d-8945-0c9d1bfb51ba">IOleInPlaceFrame</a>



<a href="https://msdn.microsoft.com/dc26a399-846d-4d15-b406-752350e528c2">IOleInPlaceFrame::SetMenu</a>



<a href="https://msdn.microsoft.com/en-us/library/ms647987(v=VS.85).aspx">InsertMenu</a>
 

 

