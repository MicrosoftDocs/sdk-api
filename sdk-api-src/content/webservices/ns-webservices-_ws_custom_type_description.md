---
UID: NS:webservices._WS_CUSTOM_TYPE_DESCRIPTION
title: "_WS_CUSTOM_TYPE_DESCRIPTION"
author: windows-sdk-content
description: Represents a custom mapping between a C data type and an XML element.
old-location: wsw\ws_custom_type_description.htm
tech.root: wsw
ms.assetid: 7ae3d16c-0755-4226-844e-52cf96fa84fb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WS_CUSTOM_TYPE_DESCRIPTION, WS_CUSTOM_TYPE_DESCRIPTION structure [Web Services for Windows], _WS_CUSTOM_TYPE_DESCRIPTION, webservices/WS_CUSTOM_TYPE_DESCRIPTION, wsw.ws_custom_type_description
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
 - WS_CUSTOM_TYPE_DESCRIPTION
product: Windows
targetos: Windows
req.typenames: WS_CUSTOM_TYPE_DESCRIPTION
req.redist: 
---

# _WS_CUSTOM_TYPE_DESCRIPTION structure


## -description


Represents a custom mapping between a C data type and an XML element.User-defined callbacks are invoked to do the actual reading and
                writing.
            


## -struct-fields




### -field size

The size of the custom type, in bytes.
                


### -field alignment

The alignment requirement of the custom type.  This must be a
                    power of two between 1 and 8.
                


### -field readCallback

A pointer to a callback which is invoked to read the type.


### -field writeCallback

A pointer to a callback which is invoked to write the type.


### -field descriptionData

This can be used to point to additional user-defined data
                    specific to the type.  It is optional and may be <b>NULL</b>.
                

The pointer to this data is passed
                    to the <a href="https://msdn.microsoft.com/95df152c-69cb-4417-9e85-e7ecb54ed042">WS_READ_TYPE_CALLBACK</a> and the
                    <a href="https://msdn.microsoft.com/f94bdf80-abea-4a97-9d41-add498e314b1">WS_WRITE_TYPE_CALLBACK</a>.  This allows the
                    callback to access information that is specific to this
                    particular usage of the callback.
                


### -field isDefaultValueCallback

 



