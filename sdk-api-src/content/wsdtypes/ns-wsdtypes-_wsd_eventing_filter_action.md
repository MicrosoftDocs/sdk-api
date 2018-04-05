---
UID: NS:wsdtypes._WSD_EVENTING_FILTER_ACTION
title: "_WSD_EVENTING_FILTER_ACTION"
author: windows-driver-content
description: Represents a boolean expression used for filtering events.
old-location: ncd\wsd_eventing_filter_action.htm
old-project: WsdApi
ms.assetid: d6fc39ec-f57a-4b20-8c8a-7e370ee3f377
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: WSD_EVENTING_FILTER_ACTION, WSD_EVENTING_FILTER_ACTION structure, _WSD_EVENTING_FILTER_ACTION, ncd.wsd_eventing_filter_action, wsdtypes/WSD_EVENTING_FILTER_ACTION
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
req.typenames: WSD_EVENTING_FILTER_ACTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WsdTypes.h
api_name:
-	WSD_EVENTING_FILTER_ACTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_EVENTING_FILTER_ACTION structure


## -description


Represents a boolean expression used for filtering events 


## -struct-fields




### -field Actions

Reference to a <a href="https://msdn.microsoft.com/86d77741-39c3-44bd-b072-d2d4eb99e488">WSD_URI_LIST</a> structure that specifies the URIs used for filtering notifications.


## -remarks



For more information about the evaluation of action filters, see Section 6.1.1, Filtering, in the <a href="http://go.microsoft.com/fwlink/p/?linkid=69499">Device Profile for Web Services</a> specification.



