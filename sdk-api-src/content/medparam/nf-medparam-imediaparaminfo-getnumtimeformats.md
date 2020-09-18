---
UID: NF:medparam.IMediaParamInfo.GetNumTimeFormats
title: IMediaParamInfo::GetNumTimeFormats (medparam.h)
description: The GetNumTimeFormats method retrieves the number of time formats that the object supports.
helpviewer_keywords: ["GetNumTimeFormats","GetNumTimeFormats method [DirectShow]","GetNumTimeFormats method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetNumTimeFormats method","IMediaParamInfo.GetNumTimeFormats","IMediaParamInfo::GetNumTimeFormats","IMediaParamInfoGetNumTimeFormats","dshow.imediaparaminfo_getnumtimeformats","medparam/IMediaParamInfo::GetNumTimeFormats"]
old-location: dshow\imediaparaminfo_getnumtimeformats.htm
tech.root: dshow
ms.assetid: 5c398554-af2b-4e7d-8f5c-1c361535e7c6
ms.date: 12/05/2018
ms.keywords: GetNumTimeFormats, GetNumTimeFormats method [DirectShow], GetNumTimeFormats method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetNumTimeFormats method, IMediaParamInfo.GetNumTimeFormats, IMediaParamInfo::GetNumTimeFormats, IMediaParamInfoGetNumTimeFormats, dshow.imediaparaminfo_getnumtimeformats, medparam/IMediaParamInfo::GetNumTimeFormats
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
 - IMediaParamInfo::GetNumTimeFormats
 - medparam/IMediaParamInfo::GetNumTimeFormats
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
 - IMediaParamInfo.GetNumTimeFormats
---

# IMediaParamInfo::GetNumTimeFormats


## -description

The <code>GetNumTimeFormats</code> method retrieves the number of time formats that the object supports.

## -parameters

### -param pdwNumTimeFormats [out]

Pointer to a variable that receives the number of supported time formats.

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