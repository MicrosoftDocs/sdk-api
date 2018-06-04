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

# ListView_MapIndexToID macro


## -description


Maps the index of an item to a unique ID. You can use this macro or send the <a href="https://msdn.microsoft.com/d0486e21-2703-4289-abb0-f5f9c7b60b40">LVM_MAPINDEXTOID</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param index

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <b>UINT</b> that contains the index of an item.


## -remarks




		List-view controls internally track items by index. This can present problems because indexes can change during the control's existence.


		You can use this macro to tag an item with an ID when you create the item. You use this ID to guarantee uniqueness during the existence of the list-view control.   
		


		To uniquely identify an item, take the index that is returned from a call such as <a href="https://msdn.microsoft.com/8143d11c-3740-4ffc-88f0-6df779c50521">IComponent::GetDisplayInfo</a> and call <a href="https://msdn.microsoft.com/d0486e21-2703-4289-abb0-f5f9c7b60b40">LVM_MAPINDEXTOID</a>. The return value is a unique ID.
		

<div class="alert"><b>Note</b>  In a multithreaded environment, you can only be sure the correct index is returned on the thread that hosts the list-view control, not on background threads.</div>
<div> </div>
To use <b>ListView_MapIndexToID</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



