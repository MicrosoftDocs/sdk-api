---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
title: WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE (wcntypes.h)
description: WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration.
helpviewer_keywords: ["WCN_VALUE_SS_CONFIGURED","WCN_VALUE_SS_NOT_CONFIGURED","WCN_VALUE_SS_RESERVED00","WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE","WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration [Windows Connect Now]","wcn.wcn_value_type_wi_fi_protected_setup_state","wcntypes/WCN_VALUE_SS_CONFIGURED","wcntypes/WCN_VALUE_SS_NOT_CONFIGURED","wcntypes/WCN_VALUE_SS_RESERVED00","wcntypes/WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE"]
old-location: wcn\wcn_value_type_wi_fi_protected_setup_state.htm
tech.root: wcn
ms.assetid: b42d6e7c-9dba-4205-97bc-0107c168b754
ms.date: 12/05/2018
ms.keywords: WCN_VALUE_SS_CONFIGURED, WCN_VALUE_SS_NOT_CONFIGURED, WCN_VALUE_SS_RESERVED00, WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE, WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration [Windows Connect Now], wcn.wcn_value_type_wi_fi_protected_setup_state, wcntypes/WCN_VALUE_SS_CONFIGURED, wcntypes/WCN_VALUE_SS_NOT_CONFIGURED, wcntypes/WCN_VALUE_SS_RESERVED00, wcntypes/WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
req.header: wcntypes.h
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
req.typenames: WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
 - wcntypes/tagWCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
 - WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
 - wcntypes/WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wcntypes.h
api_name:
 - WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE
---

# WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE enumeration


## -description

The <b>WCN_VALUE_TYPE_WI_FI_PROTECTED_SETUP_STATE</b> enumeration defines values that indicate if a device is configured.

## -enum-fields

### -field WCN_VALUE_SS_RESERVED00:0

This value is reserved.

### -field WCN_VALUE_SS_NOT_CONFIGURED:0x1

The device is not configured.

### -field WCN_VALUE_SS_CONFIGURED:0x2

The device is configured.

## -remarks

A device is considered 'not configured' if it is using factory default wireless settings. If the wireless settings have been customized by the user, the device is considered to be 'configured'. A factory reset will restore the device to a 'not configured' state.

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
