---
UID: NS:webservices._WS_LISTENER_PROPERTIES
title: "_WS_LISTENER_PROPERTIES"
author: windows-sdk-content
description: Specifies a set of WS_LISTENER_PROPERTY structures.
old-location: wsw\ws_listener_properties.htm
old-project: wsw
ms.assetid: 19619c20-d287-42d8-9326-15c810619f22
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_LISTENER_PROPERTIES, WS_LISTENER_PROPERTIES structure [Web Services for Windows], _WS_LISTENER_PROPERTIES, webservices/WS_LISTENER_PROPERTIES, wsw.ws_listener_properties
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
req.typenames: WS_LISTENER_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_LISTENER_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_LISTENER_PROPERTIES structure


## -description



                Specifies a set of <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY</a> structures.
            


## -struct-fields




### -field properties


                    An array of properties.  The number of elements in the array is specified
                    using the <b>propertyCount</b> member.  This field may be <b>NULL</b> if the propertyCount
                    is 0.
                


### -field propertyCount


                    The number of elements in the properties array.
                

