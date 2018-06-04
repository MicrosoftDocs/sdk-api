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

# _HD_LAYOUT structure


## -description


Contains information used to set the size and position of a header control. <b>HDLAYOUT</b> is used with the <a href="https://msdn.microsoft.com/0763e483-f01d-4739-8c61-1c52d1aad0b4">HDM_LAYOUT</a> message. This structure supersedes the 
			<b>HD_LAYOUT</b> structure. 


## -struct-fields




### -field prc

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

Structure that contains the coordinates of a rectangle that the header control will occupy. 


### -field pwpos

Type: <b><a href="https://msdn.microsoft.com/5a4c4a59-c1b0-4401-aa8c-7168b1029fd0">WINDOWPOS</a>*</b>

Structure that receives information about the appropriate size and position of the header control. 

