---
UID: NF:webservices.WsReadToStartElement
title: WsReadToStartElement function
author: windows-sdk-content
description: Advances the reader to the next start element skipping whitespace and comments if necessary. Optionally, it may also verify the localName and namespace of the element.
old-location: wsw\wsreadtostartelement.htm
old-project: wsw
ms.assetid: 919a3836-6a26-4d47-b123-24856b20566d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WsReadToStartElement, WsReadToStartElement function [Web Services for Windows], webservices/WsReadToStartElement, wsw.wsreadtostartelement
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsReadToStartElement
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
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
          <b>WS_E_INVALID_FORMAT</b>. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


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
      

<pre class="syntax" xml:space="preserve"><code>&lt;!-- A purchase order --&gt;
        &lt;PurchaseOrder xmlns='http://tempuri.org'&gt;
            &lt;Item&gt;
                Pencil
            &lt;/Item&gt;
        &lt;/PurchaseOrder&gt;
</code></pre>
The following examples illustrates the behaviors of <b>WsReadToStartElement</b> when the reader is
        positioned in various places in the document.
      

<pre class="syntax" xml:space="preserve"><code>WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING item = WS_XML_STRING_VALUE("Item");
WS_XML_STRING ns = WS_XML_STRING("http://tempuri.org");
WS_ERROR* error = NULL;

// Example 1: Reader on comment, element has specified name and namespace, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, &amp;purchaseOrder, &amp;ns, NULL, error);
// hr = NOERROR, the reader is positioned on &lt;PurchaseOrder&gt;

// Example 2: Reader on comment, element has specified name and namespace, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, &amp;purchaseOrder, &amp;ns, found, error);
// hr = NOERROR, found = TRUE, the reader is positioned on &lt;PurchaseOrder&gt;

// Example 3: Reader on comment, element does not have specified name and namespace, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, &amp;item, &amp;ns, NULL, error);
// hr = WS_E_INVALID_FORMAT, the reader is faulted

// Example 4: Reader on comment, element does not have specified name and namespace, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, &amp;item, &amp;ns, &amp;found, error);
// hr = NOERROR, found = FALSE, the reader is positioned on &lt;PurchaseOrder&gt;

// Example 5: Reader on comment, name and namespace not specified, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, &amp;found, error);
// hr = NOERROR, found = TRUE, the reader is positioned on &lt;PurchaseOrder&gt;

// Example 6: Reader on &lt;/Item&gt;, name and namespace not specified, found argument is not provided
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, NULL, error);
// hr = WS_E_INVALID_FORMAT, the reader is faulted

// Example 7: Reader on &lt;/Item&gt;, name and namespace not specified, found argument is provided
BOOL found;
HRESULT hr = WsReadToStartElement(reader, NULL, NULL, &amp;found, error);
// hr = NOERROR, found = FALSE, the reader is positioned on &lt;/Item&gt;
</code></pre>
If <b>WsReadToStartElement</b> indicates an element has been found, then <a href="https://msdn.microsoft.com/88661ae5-2112-4a41-8fcd-03c74f6ec170">WsReadStartElement</a> 
        or <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a> may be used to move the reader past the start element into the content of the element.
      


<a href="https://msdn.microsoft.com/90eda6f1-dda2-4595-90f5-029768278f5b">WsSkipNode</a> may be used to skip the element and all its children leaving the reader positioned on
        the <a href="https://msdn.microsoft.com/98c40d57-ee71-40f8-9416-5b29adc30489">WS_XML_NODE</a> following the corresponding end element.
      

This function can fail for any of the reasons listed in <a href="https://msdn.microsoft.com/60dacf3e-ebde-4247-be58-835565874ab6">WsReadNode</a>.
      



