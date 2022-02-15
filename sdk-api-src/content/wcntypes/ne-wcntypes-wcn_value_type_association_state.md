---
UID: NE:wcntypes.tagWCN_VALUE_TYPE_ASSOCIATION_STATE
title: WCN_VALUE_TYPE_ASSOCIATION_STATE (wcntypes.h)
description: WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration defines the possible association states of a wireless station during a Discovery request.
helpviewer_keywords: ["WCN_VALUE_AS_ASSOCIATION_FAILURE","WCN_VALUE_AS_CONFIGURATION_FAILURE","WCN_VALUE_AS_CONNECTION_SUCCESS","WCN_VALUE_AS_IP_FAILURE","WCN_VALUE_AS_NOT_ASSOCIATED","WCN_VALUE_TYPE_ASSOCIATION_STATE","WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration [Windows Connect Now]","wcn.wcn_value_type_association_state","wcntypes/WCN_VALUE_AS_ASSOCIATION_FAILURE","wcntypes/WCN_VALUE_AS_CONFIGURATION_FAILURE","wcntypes/WCN_VALUE_AS_CONNECTION_SUCCESS","wcntypes/WCN_VALUE_AS_IP_FAILURE","wcntypes/WCN_VALUE_AS_NOT_ASSOCIATED","wcntypes/WCN_VALUE_TYPE_ASSOCIATION_STATE"]
old-location: wcn\wcn_value_type_association_state.htm
tech.root: wcn
ms.assetid: 0e225d34-d58e-49ae-8642-7070e3906fb3
ms.date: 12/05/2018
ms.keywords: WCN_VALUE_AS_ASSOCIATION_FAILURE, WCN_VALUE_AS_CONFIGURATION_FAILURE, WCN_VALUE_AS_CONNECTION_SUCCESS, WCN_VALUE_AS_IP_FAILURE, WCN_VALUE_AS_NOT_ASSOCIATED, WCN_VALUE_TYPE_ASSOCIATION_STATE, WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration [Windows Connect Now], wcn.wcn_value_type_association_state, wcntypes/WCN_VALUE_AS_ASSOCIATION_FAILURE, wcntypes/WCN_VALUE_AS_CONFIGURATION_FAILURE, wcntypes/WCN_VALUE_AS_CONNECTION_SUCCESS, wcntypes/WCN_VALUE_AS_IP_FAILURE, wcntypes/WCN_VALUE_AS_NOT_ASSOCIATED, wcntypes/WCN_VALUE_TYPE_ASSOCIATION_STATE
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
req.typenames: WCN_VALUE_TYPE_ASSOCIATION_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagWCN_VALUE_TYPE_ASSOCIATION_STATE
 - wcntypes/tagWCN_VALUE_TYPE_ASSOCIATION_STATE
 - WCN_VALUE_TYPE_ASSOCIATION_STATE
 - wcntypes/WCN_VALUE_TYPE_ASSOCIATION_STATE
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
 - WCN_VALUE_TYPE_ASSOCIATION_STATE
---

# WCN_VALUE_TYPE_ASSOCIATION_STATE enumeration


## -description

The <b>WCN_VALUE_TYPE_ASSOCIATION_STATE</b> enumeration defines the possible association states of a wireless station during a Discovery request.

## -enum-fields

### -field WCN_VALUE_AS_NOT_ASSOCIATED:0

The wireless station is not associated.

### -field WCN_VALUE_AS_CONNECTION_SUCCESS:1

The connection was successfully established.

### -field WCN_VALUE_AS_CONFIGURATION_FAILURE:2

The wireless station is not properly configured.

### -field WCN_VALUE_AS_ASSOCIATION_FAILURE:3

Association has failed.

### -field WCN_VALUE_AS_IP_FAILURE:4

 The specified IP address could not be connected to, and may be invalid.

## -see-also

<a href="/windows/desktop/api/wcntypes/ne-wcntypes-wcn_attribute_type">WCN_ATTRIBUTE_TYPE</a>
