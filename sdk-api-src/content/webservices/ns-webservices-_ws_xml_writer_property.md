---
UID: NS:webservices._WS_XML_WRITER_PROPERTY
title: "_WS_XML_WRITER_PROPERTY"
author: windows-sdk-content
description: Specifies a writer specific setting.
old-location: wsw\ws_xml_writer_property.htm
old-project: wsw
ms.assetid: 2979d038-f0a8-407d-bf8e-dca4027f6410
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_XML_WRITER_PROPERTY, WS_XML_WRITER_PROPERTY structure [Web Services for Windows], _WS_XML_WRITER_PROPERTY, webservices/WS_XML_WRITER_PROPERTY, wsw.ws_xml_writer_property
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WS_XML_WRITER_PROPERTY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_WRITER_PROPERTY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_WRITER_PROPERTY structure


## -description



        Specifies a writer specific setting.
      


## -struct-fields




### -field id


          Identifies the <a href="https://msdn.microsoft.com/c919eb01-bd15-4583-afcf-e46ac2fc9c8c">WS_XML_WRITER_PROPERTY_ID</a>.
        


### -field value


            A pointer to the value to set.
            The pointer must have an alignment compatible with the type
            of the property.
        


### -field valueSize


          The size in bytes of the memory pointed to by value.
        

