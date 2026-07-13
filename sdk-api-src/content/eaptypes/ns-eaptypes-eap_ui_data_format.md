---
UID: NS:eaptypes.EAP_UI_DATA_FORMAT
title: EAP_UI_DATA_FORMAT (eaptypes.h)
description: The EAP_UI_DATA_FORMAT union specifies the value of the attribute stored in the pbUiData member of the EAP_INTERACTIVE_UI_DATA structure.
helpviewer_keywords: ["EAP_UI_DATA_FORMAT","EAP_UI_DATA_FORMAT union [EAPHost]","eaphost.eap_ui_data_format","eaptypes/EAP_UI_DATA_FORMAT"]
old-location: eaphost\eap_ui_data_format.htm
tech.root: eaphost
ms.assetid: e4b49cbd-b50d-474c-b6b5-8ff858eca424
ms.date: 12/05/2018
ms.keywords: EAP_UI_DATA_FORMAT, EAP_UI_DATA_FORMAT union [EAPHost], eaphost.eap_ui_data_format, eaptypes/EAP_UI_DATA_FORMAT
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
req.typenames: EAP_UI_DATA_FORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - eaptypes/EAP_UI_DATA_FORMAT
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
 - EAP_UI_DATA_FORMAT
---

# EAP_UI_DATA_FORMAT structure overview


## -description

The <b>EAP_UI_DATA_FORMAT</b> union specifies the value of the attribute stored in the <i>pbUiData</i> member of the <a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type">EAP_INTERACTIVE_UI_DATA</a> structure. The structure of the <b>EAP_UI_DATA_FORMAT</b> union depends on the value of <i>dwDataType</i> as specified in <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a>.

## -struct-fields

### -field credData

case(<i>EapCredReq</i>)

If [EAP_CRED_REQ](/windows/win32/eaphost/eap-cred-req)structure. 

 


case(<i>EapCredResp</i>)

If [EAP_CRED_RESP](/windows/win32/eaphost/eap-cred-resp) structure

### -field case

### -field case.EapCredReq

### -field case.EapCredResp

### -field credExpiryData

case(<i>eapCredExpiryReq</i>)

If <i>dwDataType</i> specifies a credential expiry request (<i>eapCredExpiryReq</i>), then the data pointed to by this parameter is defined by <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req">EAP_CRED_EXPIRY_REQ </a> structure.

case(<i>eapCredExpiryResp</i>)

If <i>dwDataType</i> specifies a credential expiry response type (<i>eapCredExpiryResp</i>), then this parameter is defined by <a href="/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a> structure

### -field case.EapCredExpiryReq

### -field case.EapCredExpiryResp

### -field credLogonData

case(<i>EapCredLogonReq</i>)

If [EAP_CRED_LOGON_REQ](/windows/win32/eaphost/eap-cred-logon-req) structure. 


case(<i>EapCredLogonResp</i>)

If [EAP_CRED_LOGON_RESP](/windows/win32/eaphost/eap-cred-logon-resp) structure

### -field case.EapCredLogonReq

### -field case.EapCredLogonResp

### -field EAP_INTERACTIVE_UI_DATA_TYPE

## -see-also

<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req">EAP_CRED_EXPIRY_REQ</a>



<a href="/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a>



[EAP_CRED_REQ](/windows/win32/eaphost/eap-cred-req)



[EAP_CRED_RESP](/windows/win32/eaphost/eap-cred-resp)



<a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a>



<a href="/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type">EAP_INTERACTIVE_UI_DATA_TYPE</a>

