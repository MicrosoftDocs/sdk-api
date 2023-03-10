---
UID: NF:functiondiscoveryapi.IFunctionInstanceCollection.GetCount
title: IFunctionInstanceCollection::GetCount (functiondiscoveryapi.h)
description: Gets the number of function instances in the collection.
helpviewer_keywords: ["GetCount","GetCount method","GetCount method","IFunctionInstanceCollection interface","IFunctionInstanceCollection interface","GetCount method","IFunctionInstanceCollection.GetCount","IFunctionInstanceCollection::GetCount","functiondiscoveryapi/IFunctionInstanceCollection::GetCount","ncd.ifunctioninstancecollection_getcount_method"]
old-location: ncd\ifunctioninstancecollection_getcount_method.htm
tech.root: ncd
ms.assetid: d74d10b1-dab1-4f7e-8dbc-434570bf9c79
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method, GetCount method,IFunctionInstanceCollection interface, IFunctionInstanceCollection interface,GetCount method, IFunctionInstanceCollection.GetCount, IFunctionInstanceCollection::GetCount, functiondiscoveryapi/IFunctionInstanceCollection::GetCount, ncd.ifunctioninstancecollection_getcount_method
req.header: functiondiscoveryapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: FunctionDiscoveryAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: FunDisc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFunctionInstanceCollection::GetCount
 - functiondiscoveryapi/IFunctionInstanceCollection::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FunDisc.dll
api_name:
 - IFunctionInstanceCollection.GetCount
---

# IFunctionInstanceCollection::GetCount


## -description

<p class="CCE_Message">[Function Discovery is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets the number of function instances in the collection.

## -parameters

### -param pdwCount [out]

The number of function instances.

## -returns

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwCount</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The <b>GetCount</b> and <a href="/windows/desktop/api/functiondiscoveryapi/nf-functiondiscoveryapi-ifunctioninstancecollection-item">Item</a> methods enables you to enumerate all of the function instances contained in a collection using a simple <b>for</b> or <b>while</b> loop.

## -see-also

<a href="/windows/desktop/api/functiondiscoveryapi/nn-functiondiscoveryapi-ifunctioninstancecollection">IFunctionInstanceCollection</a>