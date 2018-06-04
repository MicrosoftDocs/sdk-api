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

# ListView_HitTest macro


## -description


Determines which list-view item, if any, is at a specified position. You can use this macro or send the <a href="https://msdn.microsoft.com/81df4ed1-30bd-4b63-9cb9-5163cb7cf52c">LVM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param pinfo

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/1906cc92-e6e6-470c-86d5-042578833391">LVHITTESTINFO</a> structure that contains the position to hit test and receives information about the results of the hit test. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

