---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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


### -param clsid




### -param catid [in]

[in] Specifies the category of this text service. This category is GUID_TFCAT_TIP_KEYBOARD, GUID_TFCAT_TIP_SPEECH, GUID_TFCAT_TIP_HANDWRITING or something in GUID_TFCAT_CATEGORY_OF_TIP. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is GUID_NULL.


### -param guidProfile [in]

[in] Specifies the GUID to identify the profile. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is GUID_NULL.


### -param hkl [in]

[in] Specifies the keyboard layout handle of this profile. If <i>dwProfileType</i> is TF_PROFILETYPE_ INPUTPROCESSOR, this is <b>NULL</b>.


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
 


#### - rclsid [in]

[in] Specifies the CLSID of the text service. If <i>dwProfileType</i> is TF_PROFILETYPE_KEYBOARDLAYOUT, this is CLSID_NULL.


## -returns



The TSF manager ignores the return value of this method.



