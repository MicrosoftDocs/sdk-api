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

# SetIScsiInitiatorNodeNameA function


## -description


The <b>SetIscsiInitiatorNodeName</b> function establishes an initiator node name for the computer. This name is utilized by  any initiator nodes on the computer that are communicating with other nodes.



## -parameters




### -param InitiatorNodeName

The initiator node name. If this parameter is <b>null</b>, initiators use a default initiator node name based upon the computer name.


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>SetIscsiInitiatorNodeName</b> routine does not verify that the format of the name in <i>InitiatorNodeName</i> is correct.

Some hardware initiator drivers can respond immediately to a change of the node name, while others must be restarted to finalize the change to the node name.





