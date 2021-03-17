---
UID: NF:wmcodecdsp.IWMResamplerProps.SetUserChannelMtx
title: IWMResamplerProps::SetUserChannelMtx (wmcodecdsp.h)
description: Specifies the channel matrix.
helpviewer_keywords: ["IWMResamplerProps interface [Media Foundation]","SetUserChannelMtx method","IWMResamplerProps.SetUserChannelMtx","IWMResamplerProps::SetUserChannelMtx","SetUserChannelMtx","SetUserChannelMtx method [Media Foundation]","SetUserChannelMtx method [Media Foundation]","IWMResamplerProps interface","codecapi.iwmresamplerpropssetuserchannelmtx","mf.iwmresamplerpropssetuserchannelmtx","wmcodecdsp/IWMResamplerProps::SetUserChannelMtx"]
old-location: mf\iwmresamplerpropssetuserchannelmtx.htm
tech.root: mf
ms.assetid: d7f225a9-c63d-4b4e-b75a-ed6156e594a0
ms.date: 12/05/2018
ms.keywords: IWMResamplerProps interface [Media Foundation],SetUserChannelMtx method, IWMResamplerProps.SetUserChannelMtx, IWMResamplerProps::SetUserChannelMtx, SetUserChannelMtx, SetUserChannelMtx method [Media Foundation], SetUserChannelMtx method [Media Foundation],IWMResamplerProps interface, codecapi.iwmresamplerpropssetuserchannelmtx, mf.iwmresamplerpropssetuserchannelmtx, wmcodecdsp/IWMResamplerProps::SetUserChannelMtx
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
 - IWMResamplerProps::SetUserChannelMtx
 - wmcodecdsp/IWMResamplerProps::SetUserChannelMtx
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
 - IWMResamplerProps.SetUserChannelMtx
---

# IWMResamplerProps::SetUserChannelMtx


## -description

Specifies the channel matrix.

## -parameters

### -param userChannelMtx [in]

Pointer to an array of floating-point values that represents a channel conversion matrix.

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

This method is equivalent to setting the <a href="/windows/desktop/medfound/mfpkey-wmresamp-channelmtx">MFPKEY_WMRESAMP_CHANNELMTX</a> property, except that the matrix is represented differently:

<ul>
<li>Values are floating point.</li>
<li>The matrix is transposed.</li>
</ul>
To convert from the integer values given in the MFPKEY_WMRESAMP_CHANNELMTX property to floating-point values, use the following formula:

<code>(float)pow(10.0,((double)Coeff)/(65536.0*20.0))</code>

where <i>Coeff</i> is an integer coefficient.

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresamplerprops">IWMResamplerProps Interface</a>