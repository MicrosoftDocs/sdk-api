---
UID: NF:wcndevice.IWCNDevice.GetAttribute
title: IWCNDevice::GetAttribute
author: windows-sdk-content
description: The IWCNDevice::GetAttribute method gets a cached attribute from the device.
old-location: wcn\iwcndevice_getattribute.htm
old-project: wcn
ms.assetid: 06a73bb5-c339-4069-853d-ab22c15c1462
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetAttribute, GetAttribute method [Windows Connect Now], GetAttribute method [Windows Connect Now],IWCNDevice interface, IWCNDevice interface [Windows Connect Now],GetAttribute method, IWCNDevice.GetAttribute, IWCNDevice::GetAttribute, wcn.iwcndevice_getattribute, wcndevice/IWCNDevice::GetAttribute
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: WCN_SESSION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WcnDevice.h
api_name:
-	IWCNDevice.GetAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWCNDevice::GetAttribute


## -description


The <b>IWCNDevice::GetAttribute</b> method gets a cached attribute  from the device.


## -parameters




### -param AttributeType [in]

A <b>WCN_ATTRIBUTE_TYPE</b>  value that represents a specific attribute value (for example,   <b>WCN_PASSWORD_TYPE</b>).


### -param dwMaxBufferSize [in]

The allocated size, in bytes, of <i>pbBuffer</i>.


### -param pbBuffer [out]

A user-allocated buffer that,  on successful return, contains the contents of the attribute.



### -param pdwBufferUsed [out]

On return, contains the size of the attribute in bytes.


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
</table>
 




## -remarks



To only query the size of an attribute, a value of 0 (zero) can be passed via <i>dwMaxBufferSize</i> and <i>pdwBufferUsed</i> will be filled appropriately.




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>



<b>WCN_ATTRIBUTE_TYPE</b>
 

 

