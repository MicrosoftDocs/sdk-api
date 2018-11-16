---
UID: NS:wsdtypes.__unnamed_struct_3
title: REQUESTBODY_Renew
author: windows-sdk-content
description: Represents a WS-Eventing Renew request message.
old-location: ncd\requestbody_renew_struct.htm
tech.root: WsdApi
ms.assetid: 2646cfb7-e372-44d2-9d4c-fa68e0d567bb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: REQUESTBODY_Renew, REQUESTBODY_Renew structure, ncd.requestbody_renew_struct, wsdtypes/REQUESTBODY_Renew
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
 - REQUESTBODY_Renew
product: Windows
targetos: Windows
req.typenames: REQUESTBODY_Renew
req.redist: 
---

# REQUESTBODY_Renew structure


## -description


Represents a WS-Eventing Renew request message.


## -struct-fields




### -field Expires

Reference to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies when the renewed subscription will expire.


### -field Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

