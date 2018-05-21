---
UID: NF:wsdxml.WSDXMLCreateContext
title: WSDXMLCreateContext function
author: windows-driver-content
description: Creates a new IWSDXMLContext object.
old-location: ncd\wsdxmlcreatecontext.htm
old-project: WsdApi
ms.assetid: fb0d8c28-1dc3-43be-a1cf-c00de6c1f43e
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSDXMLCreateContext, WSDXMLCreateContext function, ncd.wsdxmlcreatecontext, wsdxml/WSDXMLCreateContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsdxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RESPONSEBODY_SubscriptionEnd
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsdApi.dll
api_name:
-	WSDXMLCreateContext
product: Windows
targetos: Windows
req.lib: WsdApi.lib
req.dll: WsdApi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSDXMLCreateContext function


## -description


Creates a new <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> 
    object.


## -parameters




### -param ppContext [out]

Pointer to a newly allocated 
      <a href="https://msdn.microsoft.com/131fa170-4c19-4a7b-82e0-e9677b7f767a">IWSDXMLContext</a> object. If the function fails, 
      this parameter can be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppContext</i> is <b>NULL</b>.

</td>
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
</table>
 



