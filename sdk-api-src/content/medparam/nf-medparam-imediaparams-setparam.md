---
UID: NF:medparam.IMediaParams.SetParam
title: IMediaParams::SetParam (medparam.h)
description: The SetParam method sets the value of a parameter.
helpviewer_keywords: ["IMediaParams interface [DirectShow]","SetParam method","IMediaParams.SetParam","IMediaParams::SetParam","IMediaParamsSetParam","SetParam","SetParam method [DirectShow]","SetParam method [DirectShow]","IMediaParams interface","dshow.imediaparams_setparam","medparam/IMediaParams::SetParam"]
old-location: dshow\imediaparams_setparam.htm
tech.root: dshow
ms.assetid: e92681d4-2c77-4c72-b3ad-f0a6be7920e2
ms.date: 12/05/2018
ms.keywords: IMediaParams interface [DirectShow],SetParam method, IMediaParams.SetParam, IMediaParams::SetParam, IMediaParamsSetParam, SetParam, SetParam method [DirectShow], SetParam method [DirectShow],IMediaParams interface, dshow.imediaparams_setparam, medparam/IMediaParams::SetParam
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
 - IMediaParams::SetParam
 - medparam/IMediaParams::SetParam
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
 - IMediaParams.SetParam
---

# IMediaParams::SetParam


## -description

The <code>SetParam</code> method sets the value of a parameter.

## -parameters

### -param dwParamIndex [in]

Zero-based index of the parameter, or DWORD_ALLPARAMS to apply the value to every parameter.

### -param value [in]

New value of the parameter.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Index out of range, or illegal parameter value.

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

If the parameter is currently within an envelope segment, the envelope segment will overwrite the new value. To remove an envelope segment, call the <a href="/windows/desktop/api/medparam/nf-medparam-imediaparams-flushenvelope">FlushEnvelope</a> method.

To enumerate the parameters supported by this object, along with their index values, use the <a href="/windows/desktop/api/medparam/nn-medparam-imediaparaminfo">IMediaParamInfo</a> interface.

## -see-also

<a href="/windows/desktop/api/medparam/nn-medparam-imediaparams">IMediaParams Interface</a>