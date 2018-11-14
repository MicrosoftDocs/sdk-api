---
UID: NF:wsdattachment.WSDCreateOutboundAttachment
title: WSDCreateOutboundAttachment function
author: windows-sdk-content
description: Creates an IWSDOutboundAttachment object.
old-location: ncd\wsdcreateoutboundattachment.htm
tech.root: WsdApi
ms.assetid: 92e4ed8a-4a17-49dd-9ed8-bc867ec8bba9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSDCreateOutboundAttachment, WSDCreateOutboundAttachment function, ncd.wsdcreateoutboundattachment, wsdattachment/WSDCreateOutboundAttachment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsdattachment.h
req.include-header: Wsdapi.h
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
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateOutboundAttachment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WSDCreateOutboundAttachment
: 
---

# WSDCreateOutboundAttachment function


## -description


Creates an <a href="https://msdn.microsoft.com/ba2f2038-e6ef-4ad4-a1fb-50e225394c60">IWSDOutboundAttachment</a> object.


## -parameters




### -param ppAttachment [out]

Returns a reference to the initialized <a href="https://msdn.microsoft.com/ba2f2038-e6ef-4ad4-a1fb-50e225394c60">IWSDOutboundAttachment</a> object. Cannot be <b>NULL</b>.


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
<i>attachmentOut</i> is <b>NULL</b>.

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
 



