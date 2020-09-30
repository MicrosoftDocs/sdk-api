---
UID: NF:medparam.IMediaParamInfo.GetCurrentTimeFormat
title: IMediaParamInfo::GetCurrentTimeFormat (medparam.h)
description: The GetCurrentTimeFormat method retrieves the current time format.
helpviewer_keywords: ["GetCurrentTimeFormat","GetCurrentTimeFormat method [DirectShow]","GetCurrentTimeFormat method [DirectShow]","IMediaParamInfo interface","IMediaParamInfo interface [DirectShow]","GetCurrentTimeFormat method","IMediaParamInfo.GetCurrentTimeFormat","IMediaParamInfo::GetCurrentTimeFormat","IMediaParamInfoGetCurrentTimeFormat","dshow.imediaparaminfo_getcurrenttimeformat","medparam/IMediaParamInfo::GetCurrentTimeFormat"]
old-location: dshow\imediaparaminfo_getcurrenttimeformat.htm
tech.root: dshow
ms.assetid: b93b929c-c1a7-4e8e-93cf-118fcd6a3de9
ms.date: 12/05/2018
ms.keywords: GetCurrentTimeFormat, GetCurrentTimeFormat method [DirectShow], GetCurrentTimeFormat method [DirectShow],IMediaParamInfo interface, IMediaParamInfo interface [DirectShow],GetCurrentTimeFormat method, IMediaParamInfo.GetCurrentTimeFormat, IMediaParamInfo::GetCurrentTimeFormat, IMediaParamInfoGetCurrentTimeFormat, dshow.imediaparaminfo_getcurrenttimeformat, medparam/IMediaParamInfo::GetCurrentTimeFormat
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
 - IMediaParamInfo::GetCurrentTimeFormat
 - medparam/IMediaParamInfo::GetCurrentTimeFormat
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
 - IMediaParamInfo.GetCurrentTimeFormat
---

# IMediaParamInfo::GetCurrentTimeFormat


## -description

The <code>GetCurrentTimeFormat</code> method retrieves the current time format.

## -parameters

### -param pguidTimeFormat [out]

Pointer to a variable that receives a time format GUID.

### -param pTimeData [out]

Pointer to a variable that receives an <b>MP_TIMEDATA</b> value specifying the unit of measure for the new format.

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

## -remarks

The meaning of the value returned in the <i>pTimeData</i> parameter depends on the time format GUID. For more information, see <a href="/windows/desktop/api/medparam/nf-medparam-imediaparams-settimeformat">IMediaParams::SetTimeFormat</a>.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo Interface</a>