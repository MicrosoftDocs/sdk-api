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

# ListView_SubItemHitTestEx macro


## -description


Determines which list-view item or subitem is located at a given position. You can use this macro or send the <a href="https://msdn.microsoft.com/1468febb-af0d-4c04-b0b1-cda5ec77aa2c">LVM_SUBITEMHITTEST</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control that will be hit-tested. 


### -param plvhti

Type: <b>LPLVHITTESTINFO</b>

A pointer to an <a href="https://msdn.microsoft.com/1906cc92-e6e6-470c-86d5-042578833391">LVHITTESTINFO</a> structure. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure within <b>LVHITTESTINFO</b> must be set to the client coordinates to be hit-tested. 


## -remarks



This macro passes -1 as the <i>wparam</i> of the message, specifying that the <b>iGroup</b> member of <i>plvhti</i> is retrieved.
	



