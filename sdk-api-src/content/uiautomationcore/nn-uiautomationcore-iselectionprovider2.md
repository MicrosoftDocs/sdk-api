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

# ISelectionProvider2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/464b05e3-06da-44b9-b4a6-c64452fcdb6d">ISelectionItemProvider</a> interface to provide information about selected items.


## -remarks



This interface is implemented by a Microsoft UI Automation provider.

Providers should raise an event of type <a href="uiauto_event_ids.htm">UIA_Selection_InvalidatedEventId</a> when a selection in a container has changed significantly.


When selecting from a list or 2D grid there are primary pieces of information that ATs would like to better read to their end users.  Using Excel as a primary example, there are 4 main pieces of information necessary for the AT to provide a good experience:  

<ul>
<li>The first cell in the selection</li>
<li>The last cell in the selection</li>
<li>The current item as you select</li>
<li>The total count</li>
</ul>
<img alt="Image of an Excel spreadsheet showing multiple cells selected. Selection starts in the upper right on cell F5 and ends in the lower left on cell D7." src="images/ISelectionPattern2.png"/>
The above image illustrates the end state of a 2D selection:


<ul>
<li>The user started in cell F5 (note this is where focus input stays because if you type that is where data lands)</li>
<li>The user selects down the column to cell F7</li>
<li>
The user then selects left to cell D7</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/464b05e3-06da-44b9-b4a6-c64452fcdb6d">ISelectionItemProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

