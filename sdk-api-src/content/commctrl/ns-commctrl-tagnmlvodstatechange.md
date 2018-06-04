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

# tagNMLVODSTATECHANGE structure


## -description


Structure that contains information for use in processing the <a href="https://msdn.microsoft.com/a3aafda5-a3ec-4f84-8153-8d34097e04f1">LVN_ODSTATECHANGED</a> notification code. 


## -struct-fields




### -field hdr

Type: <b><a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a></b>


<a href="https://msdn.microsoft.com/0c8b116b-82ad-495a-b19d-8c172e0b2608">NMHDR</a> structure that contains additional information about the notification. 


### -field iFrom

Type: <b>int</b>

Zero-based index of the first item in the range of items. 


### -field iTo

Type: <b>int</b>

Zero-based index of the last item in the range of items. 


### -field uNewState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value indicating the new state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">list-view item states</a>. 


### -field uOldState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value indicating the old state for the item or items. This member can be any valid combination of the <a href="https://msdn.microsoft.com/21827f4a-f133-489b-bbd2-6979d1928b40">list-view item states</a>. 

