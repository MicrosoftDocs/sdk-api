---
UID: NS:wsdtypes._WSD_EVENTING_EXPIRES
title: WSD_EVENTING_EXPIRES
author: windows-sdk-content
description: Represents the expiration time of a WS-Eventing message.
old-location: ncd\wsd_eventing_expires.htm
tech.root: wsdapi
ms.assetid: 728eacdb-3c27-4884-a9ba-34979590a57c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSD_EVENTING_EXPIRES, WSD_EVENTING_EXPIRES structure, ncd.wsd_eventing_expires, wsdtypes/WSD_EVENTING_EXPIRES
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
 - WSD_EVENTING_EXPIRES
product: Windows
targetos: Windows
req.typenames: WSD_EVENTING_EXPIRES
req.redist: 
---

# WSD_EVENTING_EXPIRES structure


## -description


Represents the expiration time of a WS-Eventing message. 


## -struct-fields




### -field Duration

Reference to a <a href="https://msdn.microsoft.com/43d4d0c5-509a-46c4-bdf6-24c3307fb811">WSD_DURATION</a> structure that specifies the length of time a request or response is valid.


### -field DateTime

Reference to a <a href="https://msdn.microsoft.com/ec42d69c-133a-4e76-bbbe-0e6978f4723a">WSD_DATETIME</a> structure that specifies the time that the request or response expires. 

