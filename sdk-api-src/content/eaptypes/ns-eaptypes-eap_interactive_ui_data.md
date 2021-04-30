---
UID: NS:eaptypes._EAP_INTERACTIVE_UI_DATA
title: EAP_INTERACTIVE_UI_DATA (eaptypes.h)
description: Contains configuration information for interactive UI components raised on an EAP supplicant.
helpviewer_keywords: ["EAP_INTERACTIVE_UI_DATA","EAP_INTERACTIVE_UI_DATA structure [EAPHost]","EAP_INTERACTIVE_UI_DATA_VERSION","eaphost.eap_interactive_ui_data","eaptypes/EAP_INTERACTIVE_UI_DATA"]
old-location: eaphost\eap_interactive_ui_data.htm
tech.root: eaphost
ms.assetid: 68141611-4a1c-409e-8ed2-3d21a76640c3
ms.date: 12/05/2018
ms.keywords: EAP_INTERACTIVE_UI_DATA, EAP_INTERACTIVE_UI_DATA structure [EAPHost], EAP_INTERACTIVE_UI_DATA_VERSION, eaphost.eap_interactive_ui_data, eaptypes/EAP_INTERACTIVE_UI_DATA
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
req.typenames: EAP_INTERACTIVE_UI_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EAP_INTERACTIVE_UI_DATA
 - eaptypes/_EAP_INTERACTIVE_UI_DATA
 - EAP_INTERACTIVE_UI_DATA
 - eaptypes/EAP_INTERACTIVE_UI_DATA
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
 - EAP_INTERACTIVE_UI_DATA
---

# EAP_INTERACTIVE_UI_DATA structure


## -description

The <b>EAP_INTERACTIVE_UI_DATA</b> structure contains configuration information for interactive UI components raised on an EAP supplicant.

## -struct-fields

### -field dwVersion

The version of this data structure.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EAP_INTERACTIVE_UI_DATA_VERSION"></a><a id="eap_interactive_ui_data_version"></a><dl>
<dt><b>EAP_INTERACTIVE_UI_DATA_VERSION</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The version of the EAP interactive UI data.

</td>
</tr>
</table>

### -field dwSize

The size of this entire structure, in bytes.

### -field dwDataType

An <a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type">EAP_INTERACTIVE_UI_DATA_TYPE</a> value that specifies the type of data pointed to by <i>pbUiData</i>.

### -field cbUiData

The size of the data pointed to by <i>pbUiData</i>, in bytes.



### -field pbUiData

A pointer to an <a href="/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-eap_ui_data_format">EAP_UI_DATA_FORMAT</a> union that contains information about specific user interface components that correspond to the type specified in <i>dwDataType</i>.

## -see-also

[EAPHost Supplicant Structures](/windows/win32/eaphost/eap-host-supplicant-structures)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req">EAP_CRED_EXPIRY_REQ</a>



<a href="/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a>



[EAP_CRED_REQ](/windows/win32/eaphost/eap-cred-req)



[EAP_CRED_RESP](/windows/win32/eaphost/eap-cred-resp)



<a href="/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-eap_ui_data_format">EAP_UI DATA_FORMAT</a>



[SSO Password Change Behavior](/windows/win32/eaphost/sso-password-change-behavior-)



[SSO and PLAP](/windows/win32/eaphost/understanding-sso-and-plap)