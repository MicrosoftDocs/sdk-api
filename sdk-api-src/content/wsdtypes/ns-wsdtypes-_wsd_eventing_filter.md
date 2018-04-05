---
UID: NS:wsdtypes._WSD_EVENTING_FILTER
title: "_WSD_EVENTING_FILTER"
author: windows-driver-content
description: Represents an event filter used in WS-Eventing Subscribe messages.
old-location: ncd\wsd_eventing_filter.htm
old-project: WsdApi
ms.assetid: e702aca8-9784-4e51-988b-f4311573c700
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_EVENTING_FILTER, WSD_EVENTING_FILTER structure, _WSD_EVENTING_FILTER, http://schemas.xmlsoap.org/ws/2006/02/devprof/Action, ncd.wsd_eventing_filter, wsdtypes/WSD_EVENTING_FILTER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSD_EVENTING_FILTER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_EVENTING_FILTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_EVENTING_FILTER structure


## -description


Represents an event filter used in WS-Eventing Subscribe messages.


## -struct-fields




### -field Dialect

Specifies the language or dialect use to represent the boolean expression used by the filter.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_Action"></a><a id="http___schemas.xmlsoap.org_ws_2006_02_devprof_action"></a><a id="HTTP___SCHEMAS.XMLSOAP.ORG_WS_2006_02_DEVPROF_ACTION"></a><dl>
<dt><b>http://schemas.xmlsoap.org/ws/2006/02/devprof/Action</b></dt>
</dl>
</td>
<td width="60%">
The boolean expression uses the Action filter dialect.

</td>
</tr>
</table>
 


### -field FilterAction

 


### -field Data

A reference to the expression used for filtering.  

