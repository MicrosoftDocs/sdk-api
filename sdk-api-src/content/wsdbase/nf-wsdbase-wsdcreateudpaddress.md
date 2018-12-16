---
UID: NF:wsdbase.WSDCreateUdpAddress
title: WSDCreateUdpAddress function
author: windows-sdk-content
description: Creates an IWSDUdpAddress object.
old-location: ncd\wsdcreateudpaddress.htm
tech.root: wsdapi
ms.assetid: 84610d5f-9b90-4830-b6d3-7b5622709668
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSDCreateUdpAddress, WSDCreateUdpAddress function, ncd.wsdcreateudpaddress, wsdbase/WSDCreateUdpAddress
ms.topic: function
req.header: wsdbase.h
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
req.lib: 
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
 - WSDCreateUdpAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSDCreateUdpAddress function


## -description


Creates an <a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a> object.


## -parameters




### -param ppAddress [in]

An <a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a> interface pointer. This parameter cannot be <b>NULL</b>.


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
<i>ppAddress</i> is <b>NULL</b>.

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
 



