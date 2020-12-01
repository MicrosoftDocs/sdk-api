---
UID: NS:eaptypes._EAP_CONFIG_INPUT_FIELD_ARRAY
title: EAP_CONFIG_INPUT_FIELD_ARRAY (eaptypes.h)
description: Contains a set of EAP_CONFIG_INPUT_FIELD_DATA structures that collectively contain the user input field data obtained from the user.
helpviewer_keywords: ["*PEAP_CONFIG_INPUT_FIELD_ARRAY","EAP_CONFIG_INPUT_FIELD_ARRAY","EAP_CONFIG_INPUT_FIELD_ARRAY structure [EAPHost]","EAP_CREDENTIAL_VERSION","EAP_CRED_LOGON_REQ","EAP_CRED_LOGON_RESP","EAP_CRED_REQ","EAP_CRED_RESP","PEAP_CONFIG_INPUT_FIELD_ARRAY","PEAP_CONFIG_INPUT_FIELD_ARRAY structure pointer [EAPHost]","eaphost.eap_config_input_field_array","eaptypes/EAP_CONFIG_INPUT_FIELD_ARRAY","eaptypes/PEAP_CONFIG_INPUT_FIELD_ARRAY"]
old-location: eaphost\eap_config_input_field_array.htm
tech.root: eaphost
ms.assetid: e8a2e934-1ded-4159-8cd8-7aeb75ce743a
ms.date: 12/05/2018
ms.keywords: '*PEAP_CONFIG_INPUT_FIELD_ARRAY, EAP_CONFIG_INPUT_FIELD_ARRAY, EAP_CONFIG_INPUT_FIELD_ARRAY structure [EAPHost], EAP_CREDENTIAL_VERSION, EAP_CRED_LOGON_REQ, EAP_CRED_LOGON_RESP, EAP_CRED_REQ, EAP_CRED_RESP, PEAP_CONFIG_INPUT_FIELD_ARRAY, PEAP_CONFIG_INPUT_FIELD_ARRAY structure pointer [EAPHost], eaphost.eap_config_input_field_array, eaptypes/EAP_CONFIG_INPUT_FIELD_ARRAY, eaptypes/PEAP_CONFIG_INPUT_FIELD_ARRAY'
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
req.typenames: EAP_CONFIG_INPUT_FIELD_ARRAY, *PEAP_CONFIG_INPUT_FIELD_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_CONFIG_INPUT_FIELD_ARRAY
 - eaptypes/_EAP_CONFIG_INPUT_FIELD_ARRAY
 - PEAP_CONFIG_INPUT_FIELD_ARRAY
 - eaptypes/PEAP_CONFIG_INPUT_FIELD_ARRAY
 - EAP_CONFIG_INPUT_FIELD_ARRAY
 - eaptypes/EAP_CONFIG_INPUT_FIELD_ARRAY
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
 - EAP_CONFIG_INPUT_FIELD_ARRAY
---

## -description

The <b>EAP_CONFIG_INPUT_FIELD_ARRAY</b> structure contains a set of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a>   structures that collectively contain the user input field data obtained from the user.

## -struct-fields

### -field dwVersion

The version of the <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a>   structures pointed to by <b>pFields</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAP_CREDENTIAL_VERSION"></a><a id="eap_credential_version"></a><dl>
<dt><b>EAP_CREDENTIAL_VERSION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The version of the EAP credentials supplied by the user.

</td>
</tr>
</table>

### -field dwNumberOfFields

The total number of elements in the array specified by  <b>pFields</b>.

### -field pFields

Pointer to an array of <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a> structures that contain specific user input data obtained from an EAP configuration dialog box.

## -remarks

The <b>EAP_CONFIG_INPUT_FIELD_ARRAY</b> structure can be employed to support Single-Sign-On (SSO).

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data">EAP_CONFIG_INPUT_FIELD_DATA</a>

[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)
