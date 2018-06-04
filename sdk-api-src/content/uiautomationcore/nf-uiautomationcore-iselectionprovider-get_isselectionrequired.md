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

# ISelectionProvider::get_IsSelectionRequired


## -description



        Indicates whether the Microsoft UI Automation provider requires at least one child element to be selected.
        

This property is read-only.


## -parameters


## -remarks



       
        This property can be dynamic. For example, the initial state of a control might 
        not have any items selected by default, meaning that <b>ISelectionProvider::IsSelectionRequired</b> is <b>FALSE</b>. 
        However, after an item is selected the control must always have at least one item selected.
		




## -see-also




<a href="https://msdn.microsoft.com/e02731f8-e58d-4c66-95bf-005cf954471c">ISelectionProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

