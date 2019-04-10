---
UID: NF:wcndevice.IWCNDevice.GetIntegerAttribute
title: IWCNDevice::GetIntegerAttribute (wcndevice.h)
author: windows-sdk-content
description: The GetIntegerAttribute method gets a cached attribute from the device as an integer.
old-location: wcn\iwcndevice_getintegerattribute.htm
tech.root: wcn
ms.assetid: 95ad3427-c8c9-4ac9-8c8e-c9bedf855a37
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetIntegerAttribute, GetIntegerAttribute method [Windows Connect Now], GetIntegerAttribute method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetIntegerAttribute method, IWCNDevice.GetIntegerAttribute, IWCNDevice::GetIntegerAttribute, wcn.iwcndevice_getintegerattribute, wcndevice/IWCNDevice::GetIntegerAttribute
ms.topic: method
req.header: wcndevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcnDevice.idl
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
 - COM
api_location:
 - WcnDevice.h
api_name:
 - IWCNDevice.GetIntegerAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWCNDevice::GetIntegerAttribute


## -description


The <a href="https://msdn.microsoft.com/4ef065be-0046-4ce6-8f81-417a4c8a550a">GetIntegerAttribute</a> method gets a cached attribute  from the device as an integer.


## -parameters




### -param AttributeType [in]

A <b>WCN_ATTRIBUTE_TYPE</b> value  that represents a specific attribute value (for example, <b>WCN_PASSWORD_TYPE</b>).


### -param puInteger [out]

Pointer to an unsigned-integer that represents the retrieved attribute value.


## -returns



This method can return one of these values.

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
The attribute was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The attribute specified is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>pbBuffer</i> is not large enough to contain the returned attribute value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_DATATYPE)</b></dt>
</dl>
</td>
<td width="60%">
This attribute cannot be expressed as an integer. For example, if it is a string.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>



<b>WCN_ATTRIBUTE_TYPE</b>
 

 

