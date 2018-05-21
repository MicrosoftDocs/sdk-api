---
UID: NS:webservices._WS_ELEMENT_DESCRIPTION
title: "_WS_ELEMENT_DESCRIPTION"
author: windows-driver-content
description: Represents a mapping between a C data type and an XML element.
old-location: wsw\ws_element_description.htm
old-project: wsw
ms.assetid: 17035b64-9b2c-40d3-bdce-45e9b132e9f1
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_ELEMENT_DESCRIPTION, WS_ELEMENT_DESCRIPTION structure [Web Services for Windows], _WS_ELEMENT_DESCRIPTION, webservices/WS_ELEMENT_DESCRIPTION, wsw.ws_element_description
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_ELEMENT_DESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_ELEMENT_DESCRIPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_ELEMENT_DESCRIPTION structure


## -description



                Represents a mapping between a C data type and an XML element.
            


## -struct-fields




### -field elementLocalName

The local name of the XML element.


### -field elementNs

The namespace of the XML element.


### -field type


                    The type that corresponds to this XML element.
                


                    Not all types support being read and written as an element.  If the
                    documentation for the <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a> indicates it supports
                    <a href="https://msdn.microsoft.com/31e4abad-d007-41ae-bf51-fa693e8b8ae5">WS_ELEMENT_TYPE_MAPPING</a>, then it can be used with this structure.
                


### -field typeDescription


                    Additional information about the type.  Each type has a different description
                    structure.  This may be <b>NULL</b>, depending on the <a href="https://msdn.microsoft.com/eb3732fd-1197-4e1c-b5b5-9a34aaa0951e">WS_TYPE</a>.
                

