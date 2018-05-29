---
UID: NF:webservices.WsWriteXmlnsAttribute
title: WsWriteXmlnsAttribute function
author: windows-sdk-content
description: Writes an Xmlns attribute to the current element.
old-location: wsw\wswritexmlnsattribute.htm
old-project: wsw
ms.assetid: 17d73228-ea3b-4212-b9f7-7dcfdd6043a3
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsWriteXmlnsAttribute, WsWriteXmlnsAttribute function [Web Services for Windows], webservices/WsWriteXmlnsAttribute, wsw.wswritexmlnsattribute
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WebServices.dll
api_name:
-	WsWriteXmlnsAttribute
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsWriteXmlnsAttribute function


## -description


Writes an Xmlns attribute to the current element.
      <a href="https://msdn.microsoft.com/da23f5e6-504c-4e93-9190-7d8c41efc0da">WsWriteStartElement</a> must be called before an attribute can be written and if the number of attributes exceeds the maximum number of attributes permitted for the writer the function returns <b>WS_E_QUOTA_EXCEEDED</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.)


## -parameters




### -param writer [in]

A pointer to the <a href="https://msdn.microsoft.com/8f413e60-8a30-492c-8f2d-80be511fee11">WS_XML_WRITER</a> object to which the Xmlns attribute is written.  The pointer must reference a valid <b>XML Writer</b> object.
                


### -param prefix [in, optional]

A WS_XML_STRING pointer to the prefix to use for the start element.  If the value referenced by this parameter is <b>NULL</b> the Writer will choose a attribute.
        


          Specifies the prefix to use for the xmlns attribute.
        


### -param ns [in]

A WS_XML_STRING pointer to the namespace to bind to the prefix.
        


### -param singleQuote [in]

Determines whether to use a single or a double quote for the attribute value.
        <div class="alert"><b>Note</b>  If <a href="https://msdn.microsoft.com/b4485490-b5e1-406c-883c-a30bfa334316">WS_XML_WRITER_BINARY_ENCODING</a> is set the quotation character is  not preserved and this
          parameter has have no effect.
        </div>
<div> </div>



### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">

The operation is not allowed due to the current state of the object.

</td>
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



The following conditions apply:<ul>
<li>If an empty prefix is specified then the default namespace is assigned.
      </li>
<li>If a <b>NULL</b> prefix is specified then the Writer chooses the appropriate prefix for the namespace.
      </li>
<li>
        If the Xmlns attribute is redundant it cannot be written.
      </li>
<li>
        If a non-empty prefix is specified with an empty namespace <b>WS_E_INVALID_FORMAT</b> is returned.
      </li>
</ul>




