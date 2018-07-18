---
UID: NF:webservices.WsCreateXmlBuffer
title: WsCreateXmlBuffer function
author: windows-sdk-content
description: Creates an XML Buffer which can be used to process XML data .
old-location: wsw\wscreatexmlbuffer.htm
old-project: wsw
ms.assetid: 4e122283-f285-4fff-b240-22e4a7476639
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsCreateXmlBuffer, WsCreateXmlBuffer function [Web Services for Windows], webservices/WsCreateXmlBuffer, wsw.wscreatexmlbuffer
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
 - WsCreateXmlBuffer
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateXmlBuffer function


## -description


Creates an <a href="https://msdn.microsoft.com/e379628b-c6f8-48b1-8109-59fb604f2bcb">XML Buffer</a> which can be used to process XML data .
      


## -parameters




### -param heap [in]

Pointer to the <a href="https://msdn.microsoft.com/1866f54f-26fc-4889-a88f-0d298a418bdc">WS_HEAP</a> structure representing the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926854">heap</a> from which to allocate memory for the returned XML buffer.
                


### -param properties

An array of <a href="https://msdn.microsoft.com/bec8d297-7f5a-4b8f-a333-9b535358c470">WS_XML_BUFFER_PROPERTY</a> structures containing optional properties for the XML buffer.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param buffer



        On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/75f1df70-4dc9-4365-9005-5eaca6688f16">WS_XML_BUFFER</a> structure representing the created XML buffer. The memory for this buffer is released when its heap is reset or released.
        


          The XML buffer is initially  empty.  


### -param error [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
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
</table>
 



