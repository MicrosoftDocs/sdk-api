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

# flow_desc structure


## -description


The 
<b>FLOW_DESC</b> structure contains flow descriptor information for RSVP.


## -struct-fields




### -field u1

Union of Tspec and flowspec information.


### -field u1.stspec

Sender Tspec, expressed as a <a href="https://msdn.microsoft.com/d7905687-1af8-4469-b8de-a2445afa90f4">SENDER_TSPEC</a> structure.


### -field u1.isflow

Integrated Services flowspec information, expressed as an <a href="https://msdn.microsoft.com/1e0cd196-f53c-4d68-a287-7a98b7215d6d">IS_FLOWSPEC</a> structure.


### -field u2

Union of sender and filterspec information.


### -field u2.stemp

Sender template for the flow, expressed as a <a href="https://msdn.microsoft.com/72d08944-7ac9-496f-a18b-e6fcddb59c56">FILTER_SPEC</a> structure.


### -field u2.fspec

Filter spec for the flow, expressed as a <a href="https://msdn.microsoft.com/72d08944-7ac9-496f-a18b-e6fcddb59c56">FILTER_SPEC</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/72d08944-7ac9-496f-a18b-e6fcddb59c56">FILTER_SPEC</a>



<a href="https://msdn.microsoft.com/1e0cd196-f53c-4d68-a287-7a98b7215d6d">IS_FLOWSPEC</a>



<a href="https://msdn.microsoft.com/d7905687-1af8-4469-b8de-a2445afa90f4">SENDER_TSPEC</a>
 

 

