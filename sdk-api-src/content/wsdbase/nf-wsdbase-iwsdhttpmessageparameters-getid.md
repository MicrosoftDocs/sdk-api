---
UID: NF:wsdbase.IWSDHttpMessageParameters.GetID
title: IWSDHttpMessageParameters::GetID (wsdbase.h)
description: Retrieves the transport ID for the current transaction.
helpviewer_keywords: ["GetID","GetID method","GetID method","IWSDHttpMessageParameters interface","IWSDHttpMessageParameters interface","GetID method","IWSDHttpMessageParameters.GetID","IWSDHttpMessageParameters::GetID","ncd.iwsdhttpmessageparameters_getid","wsdbase/IWSDHttpMessageParameters::GetID"]
old-location: ncd\iwsdhttpmessageparameters_getid.htm
tech.root: ncd
ms.assetid: fbe7000f-271a-4939-814d-3696d29f7a41
ms.date: 12/05/2018
ms.keywords: GetID, GetID method, GetID method,IWSDHttpMessageParameters interface, IWSDHttpMessageParameters interface,GetID method, IWSDHttpMessageParameters.GetID, IWSDHttpMessageParameters::GetID, ncd.iwsdhttpmessageparameters_getid, wsdbase/IWSDHttpMessageParameters::GetID
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
 - IWSDHttpMessageParameters::GetID
 - wsdbase/IWSDHttpMessageParameters::GetID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDHttpMessageParameters.GetID
---

# IWSDHttpMessageParameters::GetID


## -description

Retrieves the transport ID for the current transaction.

## -parameters

### -param ppszId [out]

Pointer used to return the transport ID for the current transaction. Do not deallocate this pointer.

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
<i>ppszId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The transport ID is not available.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpmessageparameters">IWSDHttpMessageParameters</a>