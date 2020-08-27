---
UID: NF:wsdbase.IWSDAddress.Deserialize
title: IWSDAddress::Deserialize (wsdbase.h)
description: Parses the address, validates its component parts and saves them in the object.
helpviewer_keywords: ["Deserialize","Deserialize method","Deserialize method","IWSDAddress interface","IWSDAddress interface","Deserialize method","IWSDAddress.Deserialize","IWSDAddress::Deserialize","ncd.iwsdaddress_deserialize","wsdbase/IWSDAddress::Deserialize"]
old-location: ncd\iwsdaddress_deserialize.htm
tech.root: ncd
ms.assetid: a23ac1cd-d2af-4562-a623-64ca1deb1830
ms.date: 12/05/2018
ms.keywords: Deserialize, Deserialize method, Deserialize method,IWSDAddress interface, IWSDAddress interface,Deserialize method, IWSDAddress.Deserialize, IWSDAddress::Deserialize, ncd.iwsdaddress_deserialize, wsdbase/IWSDAddress::Deserialize
f1_keywords:
- wsdbase/IWSDAddress.Deserialize
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
- wsdapi.dll
api_name:
- IWSDAddress.Deserialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDAddress::Deserialize


## -description


Parses the address, validates its component parts and saves them in the object.


## -parameters




### -param pszBuffer [in]

Address to save in the object.


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
<i>pszBuffer</i> is <b>NULL</b>, its length in characters exceeds WSD_MAX_TEXT_LENGTH (8192), or it does not contain an address in a valid format.

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




<a href="https://docs.microsoft.com/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a>
 

 

