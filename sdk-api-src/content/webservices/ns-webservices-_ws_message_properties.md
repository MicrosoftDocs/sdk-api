---
UID: NS:webservices._WS_MESSAGE_PROPERTIES
title: "_WS_MESSAGE_PROPERTIES"
author: windows-sdk-content
description: Specifies a set of WS_MESSAGE_PROPERTY structures.
old-location: wsw\ws_message_properties.htm
old-project: wsw
ms.assetid: 74ad74fd-457a-4408-8032-15d365f98b14
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_MESSAGE_PROPERTIES, WS_MESSAGE_PROPERTIES structure [Web Services for Windows], _WS_MESSAGE_PROPERTIES, webservices/WS_MESSAGE_PROPERTIES, wsw.ws_message_properties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_MESSAGE_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_MESSAGE_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_MESSAGE_PROPERTIES structure


## -description


Specifies a set of <a href="https://msdn.microsoft.com/40751692-a8e6-4aa6-8dc9-55308b129a94">WS_MESSAGE_PROPERTY</a> structures.
            


## -struct-fields




### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.
                


### -field propertyCount

The number of elements in the properties array.
                

