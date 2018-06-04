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

# WMPContextMenuInfo structure


## -description


The <b>WMPContextMenuInfo</b> structure contains data about a context menu command.
<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div><div> </div>

## -struct-fields




### -field dwID

The ID of the command.


### -field bstrMenuText

The menu text to display for the command.


### -field bstrHelpText

The help text to display for the command.


## -remarks



This structure is retrieved by a call to <a href="https://msdn.microsoft.com/bc6dfd97-50bb-438c-9cd6-3eac91e99cab">IWMPContentPartner::GetCommands</a>.




## -see-also




<a href="https://msdn.microsoft.com/e1aff1a3-cf24-4292-afcd-92e77b178a3a">Structures for Type 1 Online Stores</a>
 

 

