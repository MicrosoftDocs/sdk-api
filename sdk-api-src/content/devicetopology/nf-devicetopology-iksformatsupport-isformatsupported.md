---
UID: NF:devicetopology.IKsFormatSupport.IsFormatSupported
title: IKsFormatSupport::IsFormatSupported (devicetopology.h)
description: The IsFormatSupported method indicates whether the audio endpoint device supports the specified audio stream format.
helpviewer_keywords: ["IKsFormatSupport interface [Core Audio]","IsFormatSupported method","IKsFormatSupport.IsFormatSupported","IKsFormatSupport::IsFormatSupported","IKsFormatSupportIsFormatSupported","IsFormatSupported","IsFormatSupported method [Core Audio]","IsFormatSupported method [Core Audio]","IKsFormatSupport interface","coreaudio.iksformatsupport_isformatsupported","devicetopology/IKsFormatSupport::IsFormatSupported"]
old-location: coreaudio\iksformatsupport_isformatsupported.htm
tech.root: CoreAudio
ms.assetid: 0f377b14-fd19-40ac-9875-9ee3bd8d51c7
ms.date: 12/05/2018
ms.keywords: IKsFormatSupport interface [Core Audio],IsFormatSupported method, IKsFormatSupport.IsFormatSupported, IKsFormatSupport::IsFormatSupported, IKsFormatSupportIsFormatSupported, IsFormatSupported, IsFormatSupported method [Core Audio], IsFormatSupported method [Core Audio],IKsFormatSupport interface, coreaudio.iksformatsupport_isformatsupported, devicetopology/IKsFormatSupport::IsFormatSupported
req.header: devicetopology.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKsFormatSupport::IsFormatSupported
 - devicetopology/IKsFormatSupport::IsFormatSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Devicetopology.h
api_name:
 - IKsFormatSupport.IsFormatSupported
---

# IKsFormatSupport::IsFormatSupported


## -description

The <b>IsFormatSupported</b> method indicates whether the audio endpoint device supports the specified audio stream format.

## -parameters

### -param pKsFormat [in]

Pointer to an audio-stream format specifier. This parameter points to a caller-allocated buffer that contains a format specifier. The specifier begins with a <a href="/windows-hardware/drivers/ddi/content/ks/ns-ks-ksdataformat">KSDATAFORMAT</a> structure that might be followed by additional format information. For more information about <b>KSDATAFORMAT</b> and format specifiers, see the Windows DDK documentation.

### -param cbFormat [in]

The size in bytes of the buffer that contains the format specifier.

### -param pbSupported [out]

Pointer to a <b>BOOL</b> variable into which the method writes a value to indicate whether the format is supported. The method writes <b>TRUE</b> if the device supports the format and <b>FALSE</b> if the device does not support the format.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Pointer <i>pKsFormat</i> or <i>pbSupported</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The format specifier is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksformatsupport">IKsFormatSupport Interface</a>