---
UID: NS:webservices._WS_XML_READER_STREAM_INPUT
title: "_WS_XML_READER_STREAM_INPUT"
author: windows-sdk-content
description: Specifies that the source of the xml should be obtained from a callback.
old-location: wsw\ws_xml_reader_stream_input.htm
tech.root: wsw
ms.assetid: 53537eb2-6b8d-443e-9453-4b39dfef1dd7
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: WS_XML_READER_STREAM_INPUT, WS_XML_READER_STREAM_INPUT structure [Web Services for Windows], _WS_XML_READER_STREAM_INPUT, webservices/WS_XML_READER_STREAM_INPUT, wsw.ws_xml_reader_stream_input
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
 - WS_XML_READER_STREAM_INPUT
product: Windows
targetos: Windows
req.typenames: WS_XML_READER_STREAM_INPUT
req.redist: 
---

# _WS_XML_READER_STREAM_INPUT structure


## -description


Specifies that the source of the xml should be obtained from a callback.
      


## -struct-fields




### -field input

The base type for all types that derive from <a href="https://msdn.microsoft.com/1e7a708d-5dcf-44ec-b781-a34946cb2844">WS_XML_READER_INPUT</a>.
        


### -field readCallback

A callback that is invoked when <a href="https://msdn.microsoft.com/1f4138a2-acc5-4f1d-8e35-544859d2fa49">WsFillReader</a> is called.
        


### -field readCallbackState

A user-defined value that will be passed back to readCallback.
        

