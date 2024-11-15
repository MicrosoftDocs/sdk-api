---
UID: NF:webservices.WsReadToStartElement
title: WsReadToStartElement function (webservices.h)
description: Advances the reader to the next start element skipping whitespace and comments if necessary. Optionally, it may also verify the localName and namespace of the element.
helpviewer_keywords: ["WsReadToStartElement","WsReadToStartElement function [Web Services for Windows]","webservices/WsReadToStartElement","wsw.wsreadtostartelement"]
old-location: wsw\wsreadtostartelement.htm
tech.root: wsw
ms.assetid: 919a3836-6a26-4d47-b123-24856b20566d
ms.date: 12/05/2018
ms.keywords: WsReadToStartElement, WsReadToStartElement function [Web Services for Windows], webservices/WsReadToStartElement, wsw.wsreadtostartelement
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsReadToStartElement
 - webservices/WsReadToStartElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadToStartElement
---

# WsReadToStartElement function


## -description

Advances the reader to the next start element skipping whitespace and comments if necessary.  Optionally, 
        it may also verify the localName and namespace of the element.

## -parameters

### -param reader [in]

The reader which is to read to the start element.

### -param localName [in, optional]

The localName name that the element should be.  If <b>NULL</b>, any localName is permitted.

### -param ns [in, optional]

The namespace that the element should be.  If <b>NULL</b>, any namespace is permitted.

### -param found

If specified then this will indicate whether an element is found and the localName and namespace, if also specified, match.
          If not specified, and an element is not found or the localName and namespace don't match, then it will return 
          <b>WS_E_INVALID_FORMAT</b>. (See <a href="/windows/desktop/wsw/windows-web-services-return-values">Windows Web Services Return Values</a>.)

### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.

## -returns

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The input data was not in the expected format or did not have the expected value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
A quota was exceeded.

</td>
</tr>
</table>

## -remarks

Consider the following XML:
      


``` syntax
<!-- A purchase order -->
        <PurchaseOrder xmlns='http://tempuri.org'>
            <Item>
                Pencil
            </Item>
        </PurchaseOrder>

```

The following examples illustrates the behaviors of <b>WsReadToStartElement</b> when the reader is
        positioned in various places in the document.
      


``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING item = WS_XML_STRING_VALUE("Item");
WS_XML_STRING ns = WS_XML_STRING("http://tempuri.org");
WS_ERROR* error = NULL;

// Example 1: Reader on comment, element has specified name and namespace, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, &purchaseOrder, &ns, NULL, error);
// hr = NOERROR, the reader is positioned on <PurchaseOrder>

// Example 2: Reader on comment, element has specified name and namespace, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, &purchaseOrder, &ns, found, error);
// hr = NOERROR, found = TRUE, the reader is positioned on <PurchaseOrder>

// Example 3: Reader on comment, element does not have specified name and namespace, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, &item, &ns, NULL, error);
// hr = WS_E_INVALID_FORMAT, the reader is faulted

// Example 4: Reader on comment, element does not have specified name and namespace, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, &item, &ns, &found, error);
// hr = NOERROR, found = FALSE, the reader is positioned on <PurchaseOrder>

// Example 5: Reader on comment, name and namespace not specified, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, &found, error);
// hr = NOERROR, found = TRUE, the reader is positioned on <PurchaseOrder>

// Example 6: Reader on </Item>, name and namespace not specified, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, NULL, error);
// hr = WS_E_INVALID_FORMAT, the reader is faulted

// Example 7: Reader on </Item>, name and namespace not specified, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, &found, error);
// hr = NOERROR, found = FALSE, the reader is positioned on </Item>

```

If <b>WsReadToStartElement</b> indicates an element has been found, then <a href="/windows/desktop/api/webservices/nf-webservices-wsreadstartelement">WsReadStartElement</a> 
        or <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a> may be used to move the reader past the start element into the content of the element.
      


<a href="/windows/desktop/api/webservices/nf-webservices-wsskipnode">WsSkipNode</a> may be used to skip the element and all its children leaving the reader positioned on
        the <a href="/windows/desktop/api/webservices/ns-webservices-ws_xml_node">WS_XML_NODE</a> following the corresponding end element.
      

This function can fail for any of the reasons listed in <a href="/windows/desktop/api/webservices/nf-webservices-wsreadnode">WsReadNode</a>.
