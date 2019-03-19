---
UID: NS:wsdtypes.__unnamed_struct_4
title: RESPONSEBODY_Renew (wsdtypes.h)
author: windows-sdk-content
description: Represents a WS-Eventing Renew response message.
old-location: ncd\responsebody_renew_struct.htm
tech.root: WsdApi
ms.assetid: 3fe288b6-bb84-4b8f-b973-b2309c60c28e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RESPONSEBODY_Renew, RESPONSEBODY_Renew structure, ncd.responsebody_renew_struct, wsdtypes/RESPONSEBODY_Renew
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
 - RESPONSEBODY_Renew
product: Windows
targetos: Windows
req.typenames: RESPONSEBODY_Renew
req.redist: 
---

# RESPONSEBODY_Renew structure


## -description


Represents a WS-Eventing Renew response message.


## -struct-fields




### -field expires

Reference to a <a href="https://msdn.microsoft.com/728eacdb-3c27-4884-a9ba-34979590a57c">WSD_EVENTING_EXPIRES</a> structure that specifies when the subscription expires.


### -field any

 




#### - Any

Reference to a <a href="https://msdn.microsoft.com/727149b4-31b0-4fd8-b0fa-eb773edb171e">WSDXML_ELEMENT</a> structure that specifies extension content allowed by the XML <b>ANY</b> keyword.

