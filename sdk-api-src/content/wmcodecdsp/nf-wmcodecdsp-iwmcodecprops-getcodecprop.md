---
UID: NF:wmcodecdsp.IWMCodecProps.GetCodecProp
title: IWMCodecProps::GetCodecProp (wmcodecdsp.h)
description: Retrieves a codec property specific to an output format.
helpviewer_keywords: ["GetCodecProp","GetCodecProp method [Media Foundation]","GetCodecProp method [Media Foundation]","IWMCodecProps interface","IWMCodecProps interface [Media Foundation]","GetCodecProp method","IWMCodecProps.GetCodecProp","IWMCodecProps::GetCodecProp","codecapi.iwmcodecpropsgetcodecprop","g_wszWMCPCodecName","g_wszWMCPSupportedVBRModes","mf.iwmcodecpropsgetcodecprop","wmcodecdsp/IWMCodecProps::GetCodecProp"]
old-location: mf\iwmcodecpropsgetcodecprop.htm
tech.root: mf
ms.assetid: 380c0beb-47a7-46e2-bf5a-cf901d7e0719
ms.date: 12/05/2018
ms.keywords: GetCodecProp, GetCodecProp method [Media Foundation], GetCodecProp method [Media Foundation],IWMCodecProps interface, IWMCodecProps interface [Media Foundation],GetCodecProp method, IWMCodecProps.GetCodecProp, IWMCodecProps::GetCodecProp, codecapi.iwmcodecpropsgetcodecprop, g_wszWMCPCodecName, g_wszWMCPSupportedVBRModes, mf.iwmcodecpropsgetcodecprop, wmcodecdsp/IWMCodecProps::GetCodecProp
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
 - IWMCodecProps::GetCodecProp
 - wmcodecdsp/IWMCodecProps::GetCodecProp
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
 - IWMCodecProps.GetCodecProp
---

# IWMCodecProps::GetCodecProp


## -description

Retrieves a codec property specific to an output format.

## -parameters

### -param dwFormat [in]

The output format to which the property applies. Set this value to the FOURCC value of the desired video format.

### -param pszName [in]

Wide-character, null-terminated string containing the property name. The properties listed in the following table are supported only through the IWMCodecProps interface.

<table>
<tr>
<th>Property name constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="g_wszWMCPCodecName"></a><a id="g_wszwmcpcodecname"></a><a id="G_WSZWMCPCODECNAME"></a><dl>
<dt><b>g_wszWMCPCodecName</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the name of the codec that is associated with the format (or FOURCC). This is an alternative to the <a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecstrings">IWMCodecStrings</a> interface.

</td>
</tr>
<tr>
<td width="40%"><a id="g_wszWMCPSupportedVBRModes"></a><a id="g_wszwmcpsupportedvbrmodes"></a><a id="G_WSZWMCPSUPPORTEDVBRMODES"></a><dl>
<dt><b>g_wszWMCPSupportedVBRModes</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the encoding modes supported by the codec. The value returned contains one or more of the following flags: 

<ul>
<li>WM_CODEC_ONEPASS_CBR </li>
<li>WM_CODEC_ONEPASS_VBR</li>
<li>WM_CODEC_TWOPASS_CBR</li>
<li>WM_CODEC_TWOPASS_VBR_UNCONSTRAINED </li>
<li>WM_CODEC_TWOPASS_VBR_PEAKCONSTRAINED </li>
</ul>
</td>
</tr>
</table>

### -param pType [out]

Address of a variable that receives the data type of the property value.

### -param pValue [out]

Address of the byte buffer that receives the property value.

### -param pdwSize [in, out]

Pointer to the size of the value buffer, in bytes. If pValue is <b>NULL</b>, the method will set this value to the size required.

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

## -see-also

<a href="/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecprops">IWMCodecProps Interface</a>