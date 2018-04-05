---
UID: NF:wsdbase.IWSDHttpMessageParameters.SetID
title: IWSDHttpMessageParameters::SetID method
author: windows-driver-content
description: Sets the transport ID for the current transaction.
old-location: ncd\iwsdhttpmessageparameters_setid.htm
old-project: WsdApi
ms.assetid: 95a05239-f1d5-4bd8-8aec-1e641397caa0
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IWSDHttpMessageParameters, IWSDHttpMessageParameters interface, SetID method, IWSDHttpMessageParameters::SetID, SetID method, SetID method, IWSDHttpMessageParameters interface, SetID,IWSDHttpMessageParameters.SetID, ncd.iwsdhttpmessageparameters_setid, ncd.iwsdhttpmessasgeparameters_setid, wsdbase/IWSDHttpMessageParameters::SetID
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
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDHttpMessageParameters.SetID
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDHttpMessageParameters::SetID method


## -description


Sets the transport ID for the current transaction.


## -parameters




### -param pszId [in]

Pointer to the desired transport ID for the current transaction.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszId</i> is <b>NULL</b> or the length in characters of <i>pszId</i> exceeds WSD_MAX_TEXT_LENGTH (8192). 

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
 




## -see-also




<a href="https://msdn.microsoft.com/fae10e9e-0c2b-4817-bd28-a4a85ca180cc">IWSDHttpMessageParameters</a>
 

 

