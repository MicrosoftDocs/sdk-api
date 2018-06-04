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

# IShellBrowser::RemoveMenusSB


## -description


Permits the container to remove any of its menu elements from the in-place composite menu and to free all associated resources.


## -parameters




### -param hmenuShared

Type: <b>HMENU</b>

A handle to the in-place composite menu that was constructed by calls to <a href="https://msdn.microsoft.com/62cbb593-7459-4a4f-96a2-3ec2287e6a26">IShellBrowser::InsertMenusSB</a> and the  <a href="https://msdn.microsoft.com/8ca7510a-e035-4ba2-98dd-57d777cae814">InsertMenu</a> function.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/92d9fcda-8ede-4f38-ad56-59c4a75fe45a">IOleInPlaceFrame::RemoveMenus</a> method.

The object should always permit the container to remove its menu elements from the composite menu before deactivating the shared user interface.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
The method is called by the object application while it is being UI-deactivated so the browser can remove its menus.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

