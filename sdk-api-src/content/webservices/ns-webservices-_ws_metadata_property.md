---
UID: NS:webservices._WS_METADATA_PROPERTY
title: "_WS_METADATA_PROPERTY"
author: windows-sdk-content
description: Specifies a metadata object setting.
old-location: wsw\ws_metadata_property.htm
old-project: wsw
ms.assetid: 72c37aa9-f9d8-4fc5-8ad8-854e01cb54f4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WS_METADATA_PROPERTY, WS_METADATA_PROPERTY structure [Web Services for Windows], _WS_METADATA_PROPERTY, webservices/WS_METADATA_PROPERTY, wsw.ws_metadata_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: WS_METADATA_PROPERTY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_METADATA_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_METADATA_PROPERTY structure


## -description


Specifies a metadata object setting.
            


## -struct-fields




### -field id

Identifies the <a href="https://msdn.microsoft.com/d3baa961-4701-4f2f-9263-5ac0266f6056">WS_METADATA_PROPERTY_ID</a>.
                


### -field value

A pointer to the value to set.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -field valueSize

The size in bytes of the memory pointed to by value.
                

