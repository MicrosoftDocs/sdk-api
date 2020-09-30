---
UID: NF:wmcodecdsp.IWMResamplerProps.SetHalfFilterLength
title: IWMResamplerProps::SetHalfFilterLength (wmcodecdsp.h)
description: Specifies the quality of the output.
helpviewer_keywords: ["IWMResamplerProps interface [Media Foundation]","SetHalfFilterLength method","IWMResamplerProps.SetHalfFilterLength","IWMResamplerProps::SetHalfFilterLength","SetHalfFilterLength","SetHalfFilterLength method [Media Foundation]","SetHalfFilterLength method [Media Foundation]","IWMResamplerProps interface","codecapi.iwmresamplerpropssethalffilterlength","mf.iwmresamplerpropssethalffilterlength","wmcodecdsp/IWMResamplerProps::SetHalfFilterLength"]
old-location: mf\iwmresamplerpropssethalffilterlength.htm
tech.root: mf
ms.assetid: ac35fafa-d1f1-4470-b4e3-0e6fce792a11
ms.date: 12/05/2018
ms.keywords: IWMResamplerProps interface [Media Foundation],SetHalfFilterLength method, IWMResamplerProps.SetHalfFilterLength, IWMResamplerProps::SetHalfFilterLength, SetHalfFilterLength, SetHalfFilterLength method [Media Foundation], SetHalfFilterLength method [Media Foundation],IWMResamplerProps interface, codecapi.iwmresamplerpropssethalffilterlength, mf.iwmresamplerpropssethalffilterlength, wmcodecdsp/IWMResamplerProps::SetHalfFilterLength
req.header: wmcodecdsp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMResamplerProps::SetHalfFilterLength
 - wmcodecdsp/IWMResamplerProps::SetHalfFilterLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcodecdsp.h
api_name:
 - IWMResamplerProps.SetHalfFilterLength
---

# IWMResamplerProps::SetHalfFilterLength


## -description

Specifies the quality of the output.

## -parameters

### -param lhalfFilterLen [in]

Specifies the quality of the output. The valid range is 1 to 60, inclusive.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

This method is equivalent to setting the <a href="/windows/desktop/medfound/mfpkey-wmresamp-filterquality">MFPKEY_WMRESAMP_FILTERQUALITY</a> property.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops">IWMResamplerProps Interface</a>