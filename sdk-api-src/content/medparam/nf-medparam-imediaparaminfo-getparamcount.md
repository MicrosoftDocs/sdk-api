---
UID: NF:medparam.IMediaParamInfo.GetParamCount
title: IMediaParamInfo::GetParamCount (medparam.h)
description: The GetParamCount method retrieves the number of parameters that the object supports.
helpviewer_keywords: ["GetParamCount","GetParamCount method [DirectShow]","GetParamCount method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetParamCount method","IMediaParamInfo.GetParamCount","IMediaParamInfo::GetParamCount","IMediaParamInfoGetParamCount","dshow.imediaparaminfo_getparamcount","medparam/IMediaParamInfo::GetParamCount"]
old-location: dshow\imediaparaminfo_getparamcount.htm
tech.root: dshow
ms.assetid: 0c518b8e-d5a7-40ba-9b10-4d23d4376890
ms.date: 12/05/2018
ms.keywords: GetParamCount, GetParamCount method [DirectShow], GetParamCount method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetParamCount method, IMediaParamInfo.GetParamCount, IMediaParamInfo::GetParamCount, IMediaParamInfoGetParamCount, dshow.imediaparaminfo_getparamcount, medparam/IMediaParamInfo::GetParamCount
req.header: medparam.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaParamInfo::GetParamCount
 - medparam/IMediaParamInfo::GetParamCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaParamInfo.GetParamCount
---

# IMediaParamInfo::GetParamCount


## -description

The <code>GetParamCount</code> method retrieves the number of parameters that the object supports.

## -parameters

### -param pdwParams [out]

Pointer to a variable that receives the number of parameters.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>