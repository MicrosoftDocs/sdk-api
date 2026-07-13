---
UID: NF:msctf.ITfInputProcessorProfileActivationSink.OnActivated
title: ITfInputProcessorProfileActivationSink::OnActivated (msctf.h)
description: The ITfInputProcessorProfileActivationSink::OnActivated method is a callback that is called when an input processor profile is activated or deactivated.
helpviewer_keywords: ["ITfInputProcessorProfileActivationSink interface [Text Services Framework]","OnActivated method","ITfInputProcessorProfileActivationSink.OnActivated","ITfInputProcessorProfileActivationSink::OnActivated","OnActivated","OnActivated method [Text Services Framework]","OnActivated method [Text Services Framework]","ITfInputProcessorProfileActivationSink interface","TF_IPSINK_FLAG_ACTIVE","TF_PROFILETYPE_INPUTPROCESSOR","TF_PROFILETYPE_KEYBOARDLAYOUT","msctf/ITfInputProcessorProfileActivationSink::OnActivated","tsf.itfinputprocessorprofileactivationsink_onactivated"]
old-location: tsf\itfinputprocessorprofileactivationsink_onactivated.htm
tech.root: TSF
ms.assetid: d171cf73-b409-4501-a956-06867c20f214
ms.date: 12/05/2018
ms.keywords: ITfInputProcessorProfileActivationSink interface [Text Services Framework],OnActivated method, ITfInputProcessorProfileActivationSink.OnActivated, ITfInputProcessorProfileActivationSink::OnActivated, OnActivated, OnActivated method [Text Services Framework], OnActivated method [Text Services Framework],ITfInputProcessorProfileActivationSink interface, TF_IPSINK_FLAG_ACTIVE, TF_PROFILETYPE_INPUTPROCESSOR, TF_PROFILETYPE_KEYBOARDLAYOUT, msctf/ITfInputProcessorProfileActivationSink::OnActivated, tsf.itfinputprocessorprofileactivationsink_onactivated
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileActivationSink::OnActivated
 - msctf/ITfInputProcessorProfileActivationSink::OnActivated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputProcessorProfileActivationSink.OnActivated
---

# ITfInputProcessorProfileActivationSink::OnActivated


## -description

The ITfInputProcessorProfileActivationSink::OnActivated method is a callback that is called when an input processor profile is activated or deactivated.

## -parameters

### -param dwProfileType [in]

[in] The type of this profile. This is one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_INPUTPROCESSOR"></a><a id="tf_profiletype_inputprocessor"></a><dl>
<dt><b>TF_PROFILETYPE_INPUTPROCESSOR</b></dt>
</dl>
</td>
<td width="60%">
This is a text service.

</td>
</tr>
<tr>
<td width="40%"><a id="TF_PROFILETYPE_KEYBOARDLAYOUT"></a><a id="tf_profiletype_keyboardlayout"></a><dl>
<dt><b>TF_PROFILETYPE_KEYBOARDLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
This is a keyboard layout.

</td>
</tr>
</table>

### -param langid [in]

[in] Specifies the language id of the profile.

### -param clsid [in]

[in] Specifies the CLSID of the text service. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is CLSID_NULL.

### -param catid [in]

[in] Specifies the category of this text service. This category is GUID_TFCAT_TIP_KEYBOARD, GUID_TFCAT_TIP_SPEECH, GUID_TFCAT_TIP_HANDWRITING or something in GUID_TFCAT_CATEGORY_OF_TIP. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is GUID_NULL.

### -param guidProfile [in]

[in] Specifies the GUID to identify the profile. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is GUID_NULL.

### -param hkl [in]

[in] Specifies the keyboard layout handle of this profile. If <i>dwProfileType</i> is TF_PROFILETYPE_INPUTPROCESSOR, this is <b>NULL</b>.

### -param dwFlags [in]

[in]

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TF_IPSINK_FLAG_ACTIVE"></a><a id="tf_ipsink_flag_active"></a><dl>
<dt><b>TF_IPSINK_FLAG_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
This is on if this profile is activated.

</td>
</tr>
</table>

## -returns

The TSF manager ignores the return value of this method.

