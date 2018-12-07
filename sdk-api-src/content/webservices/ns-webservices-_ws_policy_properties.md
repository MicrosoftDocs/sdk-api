---
UID: NS:webservices._WS_POLICY_PROPERTIES
title: "_WS_POLICY_PROPERTIES"
author: windows-sdk-content
description: Specifies a set of WS_POLICY_PROPERTY structures.
old-location: wsw\ws_policy_properties.htm
tech.root: wsw
ms.assetid: e03f94d9-aeeb-40df-a367-c80e831125e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_POLICY_PROPERTIES, WS_POLICY_PROPERTIES structure [Web Services for Windows], _WS_POLICY_PROPERTIES, webservices/WS_POLICY_PROPERTIES, wsw.ws_policy_properties
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_POLICY_PROPERTIES
product: Windows
targetos: Windows
req.typenames: WS_POLICY_PROPERTIES
req.redist: 
---

# _WS_POLICY_PROPERTIES structure


## -description


Specifies a set of <a href="https://msdn.microsoft.com/a897eb6c-d527-46ec-a710-252679001185">WS_POLICY_PROPERTY</a> structures.
            


## -struct-fields




### -field properties

An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.
                


### -field propertyCount

The number of elements in the properties array.
                

