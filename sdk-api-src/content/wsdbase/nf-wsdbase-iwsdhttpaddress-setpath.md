---
UID: NF:wsdbase.IWSDHttpAddress.SetPath
title: IWSDHttpAddress::SetPath (wsdbase.h)
description: Sets the URI path for this address.helpviewer_keywords: ["IWSDHttpAddress interface","SetPath method","IWSDHttpAddress.SetPath","IWSDHttpAddress::SetPath","SetPath","SetPath method","SetPath method","IWSDHttpAddress interface","ncd.iwsdhttpaddress_setpath","wsdbase/IWSDHttpAddress::SetPath"]
old-location: ncd\iwsdhttpaddress_setpath.htm
tech.root: WsdApi
ms.assetid: 4bad84a6-f321-4275-9787-f6bae83c807e
ms.date: 12/05/2018
ms.keywords: IWSDHttpAddress interface,SetPath method, IWSDHttpAddress.SetPath, IWSDHttpAddress::SetPath, SetPath, SetPath method, SetPath method,IWSDHttpAddress interface, ncd.iwsdhttpaddress_setpath, wsdbase/IWSDHttpAddress::SetPath
f1_keywords:
- wsdbase/IWSDHttpAddress.SetPath
dev_langs:
- c++
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
- IWSDHttpAddress.SetPath
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDHttpAddress::SetPath


## -description


Sets the URI path for this address.


## -parameters




### -param pszPath [in]

The URI path to use for this address.


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
The length in characters of <i>pszPath</i> exceeds WSD_MAX_TEXT_LENGTH (8192). 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdhttpaddress">IWSDHttpAddress</a>
 

 

