---
UID: NS:wsdtypes.__unnamed_struct_6
title: RESPONSEBODY_GetStatus
author: windows-sdk-content
description: Represents a WS-Eventing GetStatus response message.
old-location: ncd\responsebody_getstatus.htm
tech.root: WsdApi
ms.assetid: 41db6c35-b722-4b46-bfc2-7bbfe50aaa0a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RESPONSEBODY_GetStatus, RESPONSEBODY_GetStatus structure, ncd.responsebody_getstatus, wsdtypes/RESPONSEBODY_GetMetadata
ms.prod: windows
ms.technology: windows-sdk
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
 - RESPONSEBODY_GetStatus
product: Windows
targetos: Windows
req.typenames: RESPONSEBODY_GetStatus
req.redist: 
---

# RESPONSEBODY_GetStatus structure


## -description


Represents a WS-Eventing GetStatus response message.


## -struct-fields




### -field expires

Reference to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription expires.


### -field any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

