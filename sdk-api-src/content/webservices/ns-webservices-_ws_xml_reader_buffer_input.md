---
UID: NS:webservices._WS_XML_READER_BUFFER_INPUT
title: "_WS_XML_READER_BUFFER_INPUT"
author: windows-sdk-content
description: Specifies that the source of the xml input is a buffer.
old-location: wsw\ws_xml_reader_buffer_input.htm
old-project: wsw
ms.assetid: 86277c29-d42f-4b6a-ba33-b836bef284e7
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WS_XML_READER_BUFFER_INPUT, WS_XML_READER_BUFFER_INPUT structure [Web Services for Windows], _WS_XML_READER_BUFFER_INPUT, webservices/WS_XML_READER_BUFFER_INPUT, wsw.ws_xml_reader_buffer_input
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
req.typenames: WS_XML_READER_BUFFER_INPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_XML_READER_BUFFER_INPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WS_XML_READER_BUFFER_INPUT structure


## -description



        Specifies that the source of the xml input is a buffer.
      


## -struct-fields




### -field input


          The base type for all types that derive from <a href="https://msdn.microsoft.com/1e7a708d-5dcf-44ec-b781-a34946cb2844">WS_XML_READER_INPUT</a>.
        


### -field encodedData


          A pointer to the bytes of data that comprise the encoded form of the xml.  The reader will not modify any of these bytes.
        


### -field encodedDataSize


          The length of the encodedData.
        

