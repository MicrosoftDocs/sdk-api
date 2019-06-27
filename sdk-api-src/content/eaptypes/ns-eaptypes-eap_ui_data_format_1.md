---
UID: NS:eaptypes.__unnamed_union_1
title: EAP_UI_DATA_FORMAT (eaptypes.h)
author: windows-sdk-content
description: The EAP_UI_DATA_FORMAT union specifies the value of the attribute stored in the pbUiData member of the EAP_INTERACTIVE_UI_DATA structure.
old-location: eaphost\eap_ui_data_format.htm
tech.root: eaphost
ms.assetid: e4b49cbd-b50d-474c-b6b5-8ff858eca424
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EAP_UI_DATA_FORMAT, EAP_UI_DATA_FORMAT union [EAPHost], eaphost.eap_ui_data_format, eaptypes/EAP_UI_DATA_FORMAT
ms.topic: struct
f1_keywords: 
 - "eaptypes/EAP_UI_DATA_FORMAT"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eaptypes.h
api_name:
 - EAP_UI_DATA_FORMAT
product: Windows
targetos: Windows
req.typenames: EAP_UI_DATA_FORMAT
req.redist: 
ms.custom: 19H1
---

# EAP_UI_DATA_FORMAT structure


## -description


The <b>EAP_UI_DATA_FORMAT</b> union specifies the value of the attribute stored in the <i>pbUiData</i> member of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ne-eaptypes-_eap_interactive_ui_data_type">EAP_INTERACTIVE_UI_DATA</a> structure. The structure of the <b>EAP_UI_DATA_FORMAT</b> union depends on the value of <i>dwDataType</i> as specified in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a>.


## -struct-fields




### -field credData

case(<i>EapCredReq</i>)

If <i>dwDataType</i> specifies a credential request type (<i>EapCredReq</i>), then the data pointed to by this parameter is defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-req">EAP_CRED_REQ </a>structure. 

 


case(<i>EapCredResp</i>)

If <i>dwDataType</i> specifies a credential response type (<i>EapCredResp</i>), then the data pointed to by this parameter is defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-resp">EAP_CRED_RESP</a> structure


### -field credExpiryData

case(<i>eapCredExpiryReq</i>)

If <i>dwDataType</i> specifies a credential expiry request (<i>eapCredExpiryReq</i>), then the data pointed to by this parameter is defined by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_cred_expiry_req">EAP_CRED_EXPIRY_REQ </a>structure.

case(<i>eapCredExpiryResp</i>)

If <i>dwDataType</i> specifies a credential expiry response type (<i>eapCredExpiryResp</i>), then this parameter is defined by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a> structure


### -field credLogonData

case(<i>EapCredLogonReq</i>)

If <i>dwDataType</i> specifies a logon credential request type (<i>EapCredLogonReq</i>),  the data pointed to by this parameter is defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-logon-req">EAP_CRED_LOGON_REQ</a> structure. 


case(<i>EapCredLogonResp</i>)

If <i>dwDataType</i> specifies a logon credential response type (<i>EapCredLogonResp</i>), the data pointed to by this parameter is defined by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-logon-resp">EAP_CRED_LOGON_RESP</a> structure



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_cred_expiry_req">EAP_CRED_EXPIRY_REQ</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb530539(v=vs.85)">EAP_CRED_EXPIRY_RESP</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-req">EAP_CRED_REQ</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/eaphost/eap-cred-resp">EAP_CRED_RESP</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ns-eaptypes-_eap_interactive_ui_data">EAP_INTERACTIVE_UI_DATA</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/eaptypes/ne-eaptypes-_eap_interactive_ui_data_type">EAP_INTERACTIVE_UI_DATA_TYPE</a>
 

 

