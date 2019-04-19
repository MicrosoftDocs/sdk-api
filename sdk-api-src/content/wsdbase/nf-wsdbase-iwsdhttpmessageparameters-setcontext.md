---
UID: NF:wsdbase.IWSDHttpMessageParameters.SetContext
title: IWSDHttpMessageParameters::SetContext (wsdbase.h)
author: windows-sdk-content
description: Sets the private transmission context for the current transaction.
old-location: ncd\iwsdhttpmessageparameters_setcontext.htm
tech.root: WsdApi
ms.assetid: 8e1bbfbe-b7a7-4235-bb2d-8ee0ef301871
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDHttpMessageParameters interface,SetContext method, IWSDHttpMessageParameters.SetContext, IWSDHttpMessageParameters::SetContext, SetContext, SetContext method, SetContext method,IWSDHttpMessageParameters interface, ncd.iwsdhttpmessageparameters_setcontext, wsdbase/IWSDHttpMessageParameters::SetContext
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
 - IWSDHttpMessageParameters.SetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpMessageParameters::SetContext


## -description


Sets the private transmission context for the current transaction.


## -parameters




### -param pContext [in]

Pointer to the desired private transmission context for the current transaction.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>
 

 

