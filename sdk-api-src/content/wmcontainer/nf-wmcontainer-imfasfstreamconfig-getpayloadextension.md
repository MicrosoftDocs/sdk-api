---
UID: NF:wmcontainer.IMFASFStreamConfig.GetPayloadExtension
title: IMFASFStreamConfig::GetPayloadExtension (wmcontainer.h)
description: Retrieves information about an existing payload extension.
helpviewer_keywords: ["5b3b831c-2218-4a76-8359-7f39cab53a57","GetPayloadExtension","GetPayloadExtension method [Media Foundation]","GetPayloadExtension method [Media Foundation]","IMFASFStreamConfig interface","IMFASFStreamConfig interface [Media Foundation]","GetPayloadExtension method","IMFASFStreamConfig.GetPayloadExtension","IMFASFStreamConfig::GetPayloadExtension","mf.imfasfstreamconfig_getpayloadextension","wmcontainer/IMFASFStreamConfig::GetPayloadExtension"]
old-location: mf\imfasfstreamconfig_getpayloadextension.htm
tech.root: mf
ms.assetid: 5b3b831c-2218-4a76-8359-7f39cab53a57
ms.date: 12/05/2018
ms.keywords: 5b3b831c-2218-4a76-8359-7f39cab53a57, GetPayloadExtension, GetPayloadExtension method [Media Foundation], GetPayloadExtension method [Media Foundation],IMFASFStreamConfig interface, IMFASFStreamConfig interface [Media Foundation],GetPayloadExtension method, IMFASFStreamConfig.GetPayloadExtension, IMFASFStreamConfig::GetPayloadExtension, mf.imfasfstreamconfig_getpayloadextension, wmcontainer/IMFASFStreamConfig::GetPayloadExtension
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFStreamConfig::GetPayloadExtension
 - wmcontainer/IMFASFStreamConfig::GetPayloadExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamConfig.GetPayloadExtension
---

# IMFASFStreamConfig::GetPayloadExtension


## -description

Retrieves information about an existing payload extension.

## -parameters

### -param wPayloadExtensionNumber [in]

The payload extension index. Valid indexes range from 0, to one less than the number of extensions obtained by calling <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount">IMFASFStreamConfig::GetPayloadExtensionCount</a>.

### -param pguidExtensionSystemID [out]

Receives a GUID that identifies the payload extension. For a list of predefined payload extensions, see <a href="/windows/desktop/medfound/asf-payload-extension-guids">ASF Payload Extension GUIDs</a>. Applications can also define custom payload extensions.

### -param pcbExtensionDataSize [out]

Receives the number of bytes added to each sample for the extension.

### -param pbExtensionSystemInfo [out]

Pointer to a buffer that receives information about this extension system. This information is the same for all samples and is stored in the content header (not in each sample). This parameter can be <b>NULL</b>. To find the required size of the buffer, set this parameter to <b>NULL</b>; the size is returned in <i>pcbExtensionSystemInfo</i>.

### -param pcbExtensionSystemInfo [in, out]

On input, specifies the size of the buffer pointed to by <i>pbExtensionSystemInfo</i>. On output, receives the required size of the <i>pbExtensionSystemInfo</i> buffer in bytes.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified in <i>pbExtensionSystemInfo</i> is too small.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
The <i>wPayloadExtensionNumber</i> parameter is out of range.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig">IMFASFStreamConfig</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension">IMFASFStreamConfig::AddPayloadExtension</a>



<a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount">IMFASFStreamConfig::GetPayloadExtensionCount</a>