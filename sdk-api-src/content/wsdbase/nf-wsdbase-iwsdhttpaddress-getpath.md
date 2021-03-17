---
UID: NF:wsdbase.IWSDHttpAddress.GetPath
title: IWSDHttpAddress::GetPath (wsdbase.h)
description: Gets the URI path for this address.
helpviewer_keywords: ["GetPath","GetPath method","GetPath method","IWSDHttpAddress interface","IWSDHttpAddress interface","GetPath method","IWSDHttpAddress.GetPath","IWSDHttpAddress::GetPath","ncd.iwsdhttpaddress_getpath","wsdbase/IWSDHttpAddress::GetPath"]
old-location: ncd\iwsdhttpaddress_getpath.htm
tech.root: ncd
ms.assetid: 5bf666d3-6f13-4607-a83a-ec71f40f00e6
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method, GetPath method,IWSDHttpAddress interface, IWSDHttpAddress interface,GetPath method, IWSDHttpAddress.GetPath, IWSDHttpAddress::GetPath, ncd.iwsdhttpaddress_getpath, wsdbase/IWSDHttpAddress::GetPath
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
 - IWSDHttpAddress::GetPath
 - wsdbase/IWSDHttpAddress::GetPath
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
 - IWSDHttpAddress.GetPath
---

# IWSDHttpAddress::GetPath


## -description

Gets the URI path for this address.

## -parameters

### -param ppszPath [out]

Pointer to the URI path for this address. Do not release this object.

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
<i>ppszPath</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a>