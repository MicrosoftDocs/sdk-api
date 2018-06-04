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

# _EVT_QUERY_FLAGS enumeration


## -description


Defines the values that specify how to return the query results and whether you are query against a channel or log file.




## -enum-fields




### -field EvtQueryChannelPath

Specifies that the query is against one or more channels. The <i>Path</i> parameter of the <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> function must specify the name of a  channel or <b>NULL</b>.


### -field EvtQueryFilePath

Specifies that the query is against one or more log files. The <i>Path</i> parameter of the <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> function must specify the full path to a log file or <b>NULL</b>.


### -field EvtQueryForwardDirection

Specifies that the events in the query result are ordered from oldest to newest. This is the default.


### -field EvtQueryReverseDirection

Specifies that the events in the query result are ordered from newest to oldest.


### -field EvtQueryTolerateQueryErrors

Specifies that <a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a> should run the query even if the part of the query generates an error (is not well formed). The service validates the syntax of the XPath query to determine if it is well formed. If the validation fails, the service parses the XPath into individual expressions. It builds a new XPath beginning with the left most expression. The service validates the expression and if it is valid, the service adds the next expression to the XPath. The service repeats this process until it finds the expression that is failing. It then uses the valid expressions that it found beginning with the leftmost expression as the XPath query (which means that you may not get the events that you expected). If no part of the XPath is valid, the <b>EvtQuery</b> call fails.


## -remarks



The EvtQueryChannelPath and EvtQueryFilePath flags are mutually exclusive. The EvtQueryForwardDirection and EvtQueryReverseDirection flags are also mutually exclusive.

You can retrieve events only in a forward direction from Debug and Analytic channels and from .evt and .etl log files.




## -see-also




<a href="https://msdn.microsoft.com/06b67ec4-74ab-47d7-b7b9-1180e7dee725">EvtQuery</a>
 

 

