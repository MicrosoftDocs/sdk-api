---
UID: NS:webservices._WS_ANY_ATTRIBUTES
title: "_WS_ANY_ATTRIBUTES"
author: windows-sdk-content
description: This type is used to store a set of attributes that have not been directly mapped to field of a structure.
old-location: wsw\ws_any_attributes.htm
old-project: wsw
ms.assetid: 6c428c99-755f-40ab-bc9e-e1a7a3d70c1d
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WS_ANY_ATTRIBUTES, WS_ANY_ATTRIBUTES structure [Web Services for Windows], _WS_ANY_ATTRIBUTES, webservices/WS_ANY_ATTRIBUTES, wsw.ws_any_attributes
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
req.typenames: WS_ANY_ATTRIBUTES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_ANY_ATTRIBUTES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ANY_ATTRIBUTES structure


## -description



                This type is used to store a set of attributes
                that have not been directly mapped to field of 
                a structure.
            


## -struct-fields




### -field attributes


                    An array of attributes.  This field may
                    be <b>NULL</b> if attributeCount is zero.
                


### -field attributeCount


                    The number of attributes in the array.
                


## -remarks




                This structure is typically used to preserve unknown attributes
                when deserializing a structure.
                See <a href="https://msdn.microsoft.com/14f4dbc6-0870-4b1c-8f6b-544f771771e8">WS_ANY_ATTRIBUTES_FIELD_MAPPING</a>
                and <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_ANY_ATTRIBUTES_TYPE</a> for more
                information.
            



