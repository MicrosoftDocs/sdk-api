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

# tagNMTTCUSTOMDRAW structure


## -description


Contains information specific to an <a href="https://msdn.microsoft.com/82939901-baed-452b-85bf-3c0c01e1f5df">NM_CUSTOMDRAW</a> notification code sent by a tooltip control. 


## -struct-fields




### -field nmcd

Type: <b><a href="https://msdn.microsoft.com/c8a990a9-fb39-46e7-a5d2-fc817ff46e1b">NMCUSTOMDRAW</a></b>


            Contains general custom draw information. 


### -field uDrawFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


            Specifies how tooltip text will be formatted when it is displayed. An application may change this field to alter the way text is drawn. This value is passed to the <a href="https://msdn.microsoft.com/fe412280-d797-4abd-8a29-107a9cd96145">DrawText</a> function internally. All values for the 
					<i>uFormat</i> parameter of <b>DrawText</b> are valid. 

