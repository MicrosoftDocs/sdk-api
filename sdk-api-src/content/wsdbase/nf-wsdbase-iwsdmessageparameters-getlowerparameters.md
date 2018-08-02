---
UID: NF:wsdbase.IWSDMessageParameters.GetLowerParameters
title: IWSDMessageParameters::GetLowerParameters
author: windows-sdk-content
description: Retrieves message parameters from the layer below this layer in the protocol stack.
old-location: ncd\iwsdmessageparameters_getlowerparameters.htm
old-project: WsdApi
ms.assetid: 24f4be83-adf4-4742-8a1e-4304870a16dc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetLowerParameters, GetLowerParameters method, GetLowerParameters method,IWSDMessageParameters interface, IWSDMessageParameters interface,GetLowerParameters method, IWSDMessageParameters.GetLowerParameters, IWSDMessageParameters::GetLowerParameters, ncd.iwsdmessageparameters_getlowerparameters, wsdbase/IWSDMessageParameters::GetLowerParameters
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDMessageParameters.GetLowerParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDMessageParameters::GetLowerParameters


## -description


Retrieves message parameters from the layer below this layer in the protocol stack. 


## -parameters




### -param ppTxParams [out]

An <a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a> interface that you use to communicate message specific information up and down the protocol stack.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method was not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fb659a5e-1f55-47a6-b22d-660975d8c0fd">IWSDMessageParameters</a>
 

 

