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

# IUpdateHistoryEntry2::get_Categories


## -description


Gets a collection of the update categories to which an update belongs.

This property is read-only.


## -parameters


## -remarks



The <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface  may require you to update Windows Update Agent (WUA). For more information, see <a href="https://msdn.microsoft.com/829112ab-b240-4cc4-8053-18b484934886">Updating Windows Update Agent</a>.

The information that this property returns is for the default user interface (UI) language of the user. If the default UI language of the user is unavailable, WUA uses the default UI language of the computer.   If the default language of the computer is unavailable, WUA uses the language that  the provider of the  update recommends.

Because there is a <a href="https://msdn.microsoft.com/25620fc2-25f2-4626-9e41-b44c305c505c">Categories</a> property of the <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface and a <b>Categories</b> property of the <a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a> interface, the information that is used by the localized properties of the <a href="https://msdn.microsoft.com/1ae4ab27-97f3-494b-acd2-991dccf56011">ICategory</a> interface depends on the WUA object that owns the <b>ICategory</b> interface. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdate</b>, it follows the localization rules of <b>IUpdate</b>. If the <b>ICategory</b> interface is returned from the <b>Categories</b> property of <b>IUpdateHistoryEntry2</b>, it follows the localization rules of <b>IUpdateHistoryEntry2</b>.




## -see-also




<a href="https://msdn.microsoft.com/99965928-17c7-4aaa-ba8c-6f3e07c7c5b7">IUpdateHistoryEntry2</a>
 

 

