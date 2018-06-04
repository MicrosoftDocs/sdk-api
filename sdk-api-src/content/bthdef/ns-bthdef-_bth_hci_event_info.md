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

# _BTH_HCI_EVENT_INFO structure


## -description


The <b>BTH_HCI_EVENT_INFO</b> structure is used in connection with obtaining WM_DEVICECHANGE messages for Bluetooth.


## -struct-fields




### -field bthAddress

Address of the remote device, in the form of a <a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BTH_ADDR</a> structure.


### -field connectionType

Type of connection. Valid values are <b>HCI_CONNECTION_TYPE_ACL</b> or <b>HCI_CONNECTION_TYPE_SCO</b>.


### -field connected

Status of the connection. If nonzero, the connection has been established. If zero, the connection has been terminated.


## -see-also




<a href="https://msdn.microsoft.com/81dd4925-7f0a-468f-b706-244ce99e91df">BTH_ADDR</a>



<a href="https://msdn.microsoft.com/ca28c9cd-a271-48fa-901c-e99e063854d5">Bluetooth and WM_DEVICECHANGE
				Messages</a>
 

 

