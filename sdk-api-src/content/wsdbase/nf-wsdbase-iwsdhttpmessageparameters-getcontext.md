---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetContext
title: IWSDHttpMessageParameters::GetContext
author: windows-sdk-content
description: Retrieves the private transmission context for the current transaction.
old-location: ncd\iwsdhttpmessageparameters_getcontext.htm
tech.root: WsdApi
ms.assetid: af93f97f-a3de-4b5c-92c5-2d4ab91e7985
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetContext, GetContext method, GetContext method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetContext method, IWSDHttpMessageParameters.GetContext, IWSDHttpMessageParameters::GetContext, ncd.iwsdhttpmessageparameters_getcontext, wsdbase/IWSDHttpMessageParameters::GetContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
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
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpMessageParameters.GetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDHttpMessageParameters::GetContext


## -description


Retrieves the private transmission context for the current transaction.


## -parameters




### -param ppContext [out]

Pointer to the pointer used to retrieve the desired private transmission context for the current transaction.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppContext</i> is NULL.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Could not retrieve the context.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>
 

 

