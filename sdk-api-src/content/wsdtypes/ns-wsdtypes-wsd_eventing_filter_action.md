---
UID: NS:wsdtypes._WSD_EVENTING_FILTER_ACTION
title: WSD_EVENTING_FILTER_ACTION (wsdtypes.h)
author: windows-sdk-content
description: Represents a boolean expression used for filtering events.
old-location: ncd\wsd_eventing_filter_action.htm
tech.root: WsdApi
ms.assetid: d6fc39ec-f57a-4b20-8c8a-7e370ee3f377
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WSD_EVENTING_FILTER_ACTION, WSD_EVENTING_FILTER_ACTION structure, ncd.wsd_eventing_filter_action, wsdtypes/WSD_EVENTING_FILTER_ACTION
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_EVENTING_FILTER_ACTION
product: Windows
targetos: Windows
req.typenames: WSD_EVENTING_FILTER_ACTION
req.redist: 
ms.custom: 19H1
---

# WSD_EVENTING_FILTER_ACTION structure


## -description


Represents a boolean expression used for filtering events 


## -struct-fields




### -field Actions

Reference to a <a href="https://docs.microsoft.com/windows/desktop/api/wsdtypes/ns-wsdtypes-_wsd_uri_list">WSD_URI_LIST</a> structure that specifies the URIs used for filtering notifications.


## -remarks



For more information about the evaluation of action filters, see Section 6.1.1, Filtering, in the <a href="http://go.microsoft.com/fwlink/p/?linkid=69499">Device Profile for Web Services</a> specification.



