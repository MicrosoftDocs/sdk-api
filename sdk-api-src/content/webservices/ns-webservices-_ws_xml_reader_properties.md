---
UID: NS:webservices._WS_XML_READER_PROPERTIES
title: "_WS_XML_READER_PROPERTIES"
author: windows-driver-content
description: A structure that is used to specify a set of WS_XML_READER_PROPERTYs.
old-location: wsw\ws_xml_reader_properties.htm
old-project: wsw
ms.assetid: 5373c8d3-9201-417e-99d9-cc0d15a35ea6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: WS_XML_READER_PROPERTIES, WS_XML_READER_PROPERTIES structure [Web Services for Windows], _WS_XML_READER_PROPERTIES, webservices/WS_XML_READER_PROPERTIES, wsw.ws_xml_reader_properties
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
req.typenames: WS_XML_READER_PROPERTIES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_READER_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_READER_PROPERTIES structure


## -description



                A structure that is used to specify a set of <a href="https://msdn.microsoft.com/8864d679-c321-45bb-b774-f05696d6098e">WS_XML_READER_PROPERTY</a>s.
            


## -struct-fields




### -field properties


                    An array of properties.  The number of elements in the array is specified
                    using the propertyCount parameter.  This field may be <b>NULL</b> if the propertyCount
                    is 0.
                


### -field propertyCount


                    The number of elements in the properties array.
                

