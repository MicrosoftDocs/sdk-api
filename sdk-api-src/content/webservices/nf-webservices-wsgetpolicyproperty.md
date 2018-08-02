---
UID: NF:webservices.WsGetPolicyProperty
title: WsGetPolicyProperty function
author: windows-sdk-content
description: Retrieves a property of a policy object.
old-location: wsw\wsgetpolicyproperty.htm
old-project: wsw
ms.assetid: eebf1729-8492-47d3-90b2-6700d886de4a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WsGetPolicyProperty, WsGetPolicyProperty function [Web Services for Windows], webservices/WsGetPolicyProperty, wsw.wsgetpolicyproperty
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
 - WsGetPolicyProperty
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsGetPolicyProperty function


## -description


Retrieves a property of a policy object.
            
            


## -parameters




### -param policy [in]

A pointer to the <a href="https://msdn.microsoft.com/04623686-5065-4e97-8685-c72f848b92ab">WS_POLICY</a> object from which to obtain the property.
                


### -param id [in]

An identifier of the policy property to retrieve.
                


### -param value

A pointer to the address to store the retrieved property value. The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.
                


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
The property id was not supported for this object or the specified buffer was not large enough for the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Ran out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks



The data returned by this function is good until the 
                metadata object is freed or reset.
            



