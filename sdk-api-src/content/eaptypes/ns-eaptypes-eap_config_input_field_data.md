---
UID: NS:eaptypes._EAP_CONFIG_INPUT_FIELD_DATA
title: EAP_CONFIG_INPUT_FIELD_DATA (eaptypes.h)
description: Contains the data associated with a single input field.
helpviewer_keywords: ["*PEAP_CONFIG_INPUT_FIELD_DATA","EAP_CONFIG_INPUT_FIELD_DATA","EAP_CONFIG_INPUT_FIELD_DATA structure [EAPHost]","EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT","EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE","EAP_CONFIG_INPUT_FIELD_PROPS_NON_PERSIST","EAP_UI_INPUT_FIELD_PROPS_DEFAULT","EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE","EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST","EAP_UI_INPUT_FIELD_PROPS_READ_ONLY","MAX_EAP_CONFIG_INPUT_FIELD_LENGTH","MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH","PEAP_CONFIG_INPUT_FIELD_DATA","PEAP_CONFIG_INPUT_FIELD_DATA structure pointer [EAPHost]","eaphost.eap_config_input_field_data","eaptypes/EAP_CONFIG_INPUT_FIELD_DATA","eaptypes/PEAP_CONFIG_INPUT_FIELD_DATA"]
old-location: eaphost\eap_config_input_field_data.htm
tech.root: eaphost
ms.assetid: 2b321f26-fb40-44e5-b483-52d85cb54c8c
ms.date: 12/05/2018
ms.keywords: '*PEAP_CONFIG_INPUT_FIELD_DATA, EAP_CONFIG_INPUT_FIELD_DATA, EAP_CONFIG_INPUT_FIELD_DATA structure [EAPHost], EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT, EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE, EAP_CONFIG_INPUT_FIELD_PROPS_NON_PERSIST, EAP_UI_INPUT_FIELD_PROPS_DEFAULT, EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE, EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST, EAP_UI_INPUT_FIELD_PROPS_READ_ONLY, MAX_EAP_CONFIG_INPUT_FIELD_LENGTH, MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH, PEAP_CONFIG_INPUT_FIELD_DATA, PEAP_CONFIG_INPUT_FIELD_DATA structure pointer [EAPHost], eaphost.eap_config_input_field_data, eaptypes/EAP_CONFIG_INPUT_FIELD_DATA, eaptypes/PEAP_CONFIG_INPUT_FIELD_DATA'
req.header: eaptypes.h
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
req.typenames: EAP_CONFIG_INPUT_FIELD_DATA, *PEAP_CONFIG_INPUT_FIELD_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_CONFIG_INPUT_FIELD_DATA
 - eaptypes/_EAP_CONFIG_INPUT_FIELD_DATA
 - PEAP_CONFIG_INPUT_FIELD_DATA
 - eaptypes/PEAP_CONFIG_INPUT_FIELD_DATA
 - EAP_CONFIG_INPUT_FIELD_DATA
 - eaptypes/EAP_CONFIG_INPUT_FIELD_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_CONFIG_INPUT_FIELD_DATA
---

# EAP_CONFIG_INPUT_FIELD_DATA structure


## -description

The <b>EAP_CONFIG_INPUT_FIELD_DATA</b> structure contains the data associated with a single input field.

## -struct-fields

### -field dwSize

The size, in bytes, of the <b>EAP_CONFIG_INPUT_FIELD_DATA</b> structure. This field is used for versioning purposes.

### -field Type

An <a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_config_input_field_type">EAP_CONFIG_INPUT_FIELD_TYPE</a> enumeration value that specifies the type of the input field.

### -field dwFlagProps

A set of flag values that describe properties of the EAP configuration input field.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAP_UI_INPUT_FIELD_PROPS_DEFAULT"></a><a id="eap_ui_input_field_props_default"></a><dl>
<dt><b>EAP_UI_INPUT_FIELD_PROPS_DEFAULT</b></dt>
<dt>0X00000000
</dt>
</dl>
</td>
<td width="60%">
Windows Vista with SP1 or later: Represents the default property value for input field entries displayed in the UI.

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT"></a><a id="eap_config_input_field_props_default"></a><dl>
<dt><b>EAP_CONFIG_INPUT_FIELD_PROPS_DEFAULT</b></dt>
<dt>0X00000000
</dt>
</dl>
</td>
<td width="60%">
Represents the default property value for configuration input field entries displayed in the UI.

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></a><a id="eap_ui_input_field_props_non_displayable"></a><dl>
<dt><b>EAP_UI_INPUT_FIELD_PROPS_NON_DISPLAYABLE</b></dt>
<dt>0X00000001
</dt>
</dl>
</td>
<td width="60%">
Windows Vista with SP1 or later: Specifies that input field entries will not be displayed in the UI (a password or PIN number, for example).

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE"></a><a id="eap_config_input_field_props_non_displayable"></a><dl>
<dt><b>EAP_CONFIG_INPUT_FIELD_PROPS_NON_DISPLAYABLE</b></dt>
<dt>0X00000001
</dt>
</dl>
</td>
<td width="60%">
Specifies that configuration input field entries will not be displayed in the UI (a password or PIN number, for example).

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST"></a><a id="eap_ui_input_field_props_non_persist"></a><dl>
<dt><b>EAP_UI_INPUT_FIELD_PROPS_NON_PERSIST</b></dt>
<dt>0X00000002
</dt>
</dl>
</td>
<td width="60%">
Windows Vista with SP1 or later: Indicates that the EAP method will not cache the field data; the supplicant must cache the field data for roaming.

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_CONFIG_INPUT_FIELD_PROPS_NON_PERSIST"></a><a id="eap_config_input_field_props_non_persist"></a><dl>
<dt><b>EAP_CONFIG_INPUT_FIELD_PROPS_NON_PERSIST</b></dt>
<dt>0X00000002
</dt>
</dl>
</td>
<td width="60%">
Indicates that the EAP method will not cache the field data; the supplicant must cache the field data for roaming.

</td>
</tr>
<tr>
<td width="40%"><a id="EAP_UI_INPUT_FIELD_PROPS_READ_ONLY"></a><a id="eap_ui_input_field_props_read_only"></a><dl>
<dt><b>EAP_UI_INPUT_FIELD_PROPS_READ_ONLY</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Windows Vista with SP1 or later: Indicates that the input field is read-only and cannot be edited.

</td>
</tr>
</table>

### -field pwszLabel

A pointer to a zero-terminated Unicode string that contains the label for the input field. The caller must free the inner pointers
                using the function <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>, starting at the innermost pointer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAX_EAP_CONFIG_INPUT_FIELD_LENGTH"></a><a id="max_eap_config_input_field_length"></a><dl>
<dt><b>MAX_EAP_CONFIG_INPUT_FIELD_LENGTH</b></dt>
<dt>256</dt>
</dl>
</td>
<td width="60%">
Specifies the maximum supported length of an input field.

</td>
</tr>
</table>

### -field pwszData

A pointer to a zero-terminated  Unicode string that contains the data entered by the user into the input field. This value is initially empty. It is populated in a Single-Sign-On (SSO) scenario and returned to EAPHost with a call to <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryuserblobfromcredentialinputfields">EapHostPeerQueryUserBlobFromCredentialInputFields</a>. The caller must free the inner pointers
                using the function EapHostPeerFreeMemory, starting at the innermost pointer.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH"></a><a id="max_eap_config_input_field_value_length"></a><dl>
<dt><b>MAX_EAP_CONFIG_INPUT_FIELD_VALUE_LENGTH</b></dt>
<dt>1024</dt>
</dl>
</td>
<td width="60%">
Specifies the maximum supported length of an input field.

</td>
</tr>
</table>

### -field dwMinDataLength

The minimum length, in bytes, allowed for data entered  by the user into the EAP configuration dialog box input field.

### -field dwMaxDataLength

The maximum length, in bytes, allowed for data entered by the user into the EAP configuration dialog box input field.

## -remarks

The <b>EAP_CONFIG_INPUT_FIELD_DATA</b> structure can be employed to support SSO.

This structure represents the data associated with a single input field in an EAP configuration dialog box. For example, it could contain the data for the "Login User" as supplied by the EAP application user.

The entire collection of input fields in a EAP configuration dialog box is represented by a <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a> structure.

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array">EAP_CONFIG_INPUT_FIELD_ARRAY</a>



<a href="/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerquerycredentialinputfields">EapPeerQueryCredentialInputFields</a>



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)