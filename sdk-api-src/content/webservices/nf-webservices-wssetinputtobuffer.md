---
UID: NF:webservices.WsSetInputToBuffer
title: WsSetInputToBuffer function (webservices.h)
author: windows-sdk-content
description: Sets Reader input to a specified XML buffer. Reader properties specified to WsSetInputToBuffer override properties set by WsCreateReader.
old-location: wsw\wssetinputtobuffer.htm
tech.root: wsw
ms.assetid: 0b3ac6ab-8c16-4189-950d-84bdcdabcde0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsSetInputToBuffer, WsSetInputToBuffer function [Web Services for Windows], webservices/WsSetInputToBuffer, wsw.wssetinputtobuffer
ms.topic: function
f1_keywords:
- webservices/WsSetInputToBuffer
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
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WebServices.dll
api_name:
- WsSetInputToBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsSetInputToBuffer function


## -description


Sets Reader input to a specified XML buffer.
      Reader properties
        specified to <b>WsSetInputToBuffer</b>  override properties set by <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wscreatereader">WsCreateReader</a>.

The reader does not modify <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-xml-buffer">WS_XML_BUFFER</a> input data.
      <div class="alert"><b>Note</b>  It is permissible for more than one reader to read from the same <b>WS_XML_BUFFER</b>.</div>
<div> </div>



## -parameters




### -param reader [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-xml-reader">WS_XML_READER</a> object for which the input will be set.
        


### -param buffer [in]

A pointer to the XML buffer to read.
        


### -param properties

A pointer that references an array of optional Reader properties.  <div class="alert"><b>Note</b>  For more information see <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_xml_reader_property">WS_XML_READER_PROPERTY</a>.</div>
<div> </div>.
        


### -param propertyCount [in]

The number of properties.


### -param error [in, optional]

A  pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When an XML Reader has an XML Buffer as an input source, the Reader can be used in a random access fashion, and
        the functions <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsgetreaderposition">WsGetReaderPosition</a>, <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wssetreaderposition">WsSetReaderPosition</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nf-webservices-wsmovereader">WsMoveReader</a> are available for use.
      



