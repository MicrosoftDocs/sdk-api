---
UID: NF:wsdbase.IWSDMessageParameters.GetLocalAddress
title: IWSDMessageParameters::GetLocalAddress (wsdbase.h)
description: Retrieves the generic address object representing the local address that received the message.
helpviewer_keywords: ["GetLocalAddress","GetLocalAddress method","GetLocalAddress method","IWSDMessageParameters interface","IWSDMessageParameters interface","GetLocalAddress method","IWSDMessageParameters.GetLocalAddress","IWSDMessageParameters::GetLocalAddress","ncd.iwsdmessageparameters_getlocaladdress","wsdbase/IWSDMessageParameters::GetLocalAddress"]
old-location: ncd\iwsdmessageparameters_getlocaladdress.htm
tech.root: ncd
ms.assetid: 97eab68f-9a77-46ae-a50e-be6267e25040
ms.date: 12/05/2018
ms.keywords: GetLocalAddress, GetLocalAddress method, GetLocalAddress method,IWSDMessageParameters interface, IWSDMessageParameters interface,GetLocalAddress method, IWSDMessageParameters.GetLocalAddress, IWSDMessageParameters::GetLocalAddress, ncd.iwsdmessageparameters_getlocaladdress, wsdbase/IWSDMessageParameters::GetLocalAddress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSDMessageParameters::GetLocalAddress
 - wsdbase/IWSDMessageParameters::GetLocalAddress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDMessageParameters.GetLocalAddress
---

# IWSDMessageParameters::GetLocalAddress


## -description

Retrieves the generic address object representing the local address that received the message.

## -parameters

### -param ppAddress [out]

An <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a> interface that represents the local address that received the message.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppAddress</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The caller is responsible for releasing memory allocated to <i>ppAddress</i>.

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdmessageparameters">IWSDMessageParameters</a>