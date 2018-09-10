---
UID: NS:lpmapi.flow_desc
title: flow_desc
author: windows-sdk-content
description: The FLOW_DESC structure contains flow descriptor information for RSVP.
old-location: qos\flow_desc.htm
tech.root: QOS
ms.assetid: 11ecd7ac-13c4-4f55-9700-105153b4fead
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FLOW_DESC, FLOW_DESC structure [QOS], flow_desc, lpmapi/FLOW_DESC, qos.flow_desc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - FLOW_DESC
product: Windows
targetos: Windows
req.typenames: FLOW_DESC
req.redist: 
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
 

 

