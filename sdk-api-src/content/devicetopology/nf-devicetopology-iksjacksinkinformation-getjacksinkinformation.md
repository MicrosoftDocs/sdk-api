---
UID: NF:devicetopology.IKsJackSinkInformation.GetJackSinkInformation
title: IKsJackSinkInformation::GetJackSinkInformation (devicetopology.h)
description: The GetJackSinkInformation method retrieves the sink information for the specified jack.
helpviewer_keywords: ["GetJackSinkInformation","GetJackSinkInformation method [Core Audio]","GetJackSinkInformation method [Core Audio]","IKsJackSinkInformation interface","IKsJackSinkInformation interface [Core Audio]","GetJackSinkInformation method","IKsJackSinkInformation.GetJackSinkInformation","IKsJackSinkInformation::GetJackSinkInformation","coreaudio.iksjacksinkinformation_getjacksinkinformation","devicetopology/IKsJackSinkInformation::GetJackSinkInformation"]
old-location: coreaudio\iksjacksinkinformation_getjacksinkinformation.htm
tech.root: CoreAudio
ms.assetid: ca4165ce-433a-4a8f-9853-bbe812de90ca
ms.date: 12/05/2018
ms.keywords: GetJackSinkInformation, GetJackSinkInformation method [Core Audio], GetJackSinkInformation method [Core Audio],IKsJackSinkInformation interface, IKsJackSinkInformation interface [Core Audio],GetJackSinkInformation method, IKsJackSinkInformation.GetJackSinkInformation, IKsJackSinkInformation::GetJackSinkInformation, coreaudio.iksjacksinkinformation_getjacksinkinformation, devicetopology/IKsJackSinkInformation::GetJackSinkInformation
req.header: devicetopology.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IKsJackSinkInformation::GetJackSinkInformation
 - devicetopology/IKsJackSinkInformation::GetJackSinkInformation
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
 - IKsJackSinkInformation.GetJackSinkInformation
---

# IKsJackSinkInformation::GetJackSinkInformation


## -description

The <b>GetJackSinkInformation</b> method retrieves the sink information for the specified jack.

## -parameters

### -param pJackSinkInformation [out]

Pointer to a caller-allocated buffer that receives the sink information of the jack in a <a href="/windows/win32/api/devicetopology/ns-devicetopology-ksjack_sink_information">KSJACK_SINK_INFORMATION</a> structure. The buffer size must be at least <code>sizeof(KSJACK_SINK_INFORMATION)</code>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nJack</i> is not a valid jack index.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>pDescription</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/devicetopology/nn-devicetopology-iksjacksinkinformation">IKsJackSinkInformation</a>