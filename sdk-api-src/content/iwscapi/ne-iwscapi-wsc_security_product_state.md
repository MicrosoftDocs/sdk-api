---
UID: NE:iwscapi.WSC_SECURITY_PRODUCT_STATE
title: WSC_SECURITY_PRODUCT_STATE (iwscapi.h)
description: Defines the current state of the security product that is made available to Windows Security Center.
helpviewer_keywords: ["WSC_SECURITY_PRODUCT_STATE","WSC_SECURITY_PRODUCT_STATE enumeration [Windows API]","WSC_SECURITY_PRODUCT_STATE_EXPIRED","WSC_SECURITY_PRODUCT_STATE_OFF","WSC_SECURITY_PRODUCT_STATE_ON","WSC_SECURITY_PRODUCT_STATE_SNOOZED","iwscapi/WSC_SECURITY_PRODUCT_STATE","iwscapi/WSC_SECURITY_PRODUCT_STATE_EXPIRED","iwscapi/WSC_SECURITY_PRODUCT_STATE_OFF","iwscapi/WSC_SECURITY_PRODUCT_STATE_ON","iwscapi/WSC_SECURITY_PRODUCT_STATE_SNOOZED","winprog.wsc_security_product_state"]
old-location: winprog\wsc_security_product_state.htm
tech.root: winprog
ms.assetid: 2783795B-4A7A-4033-A9EE-9B4CEF2E61B9
ms.date: 12/05/2018
ms.keywords: WSC_SECURITY_PRODUCT_STATE, WSC_SECURITY_PRODUCT_STATE enumeration [Windows API], WSC_SECURITY_PRODUCT_STATE_EXPIRED, WSC_SECURITY_PRODUCT_STATE_OFF, WSC_SECURITY_PRODUCT_STATE_ON, WSC_SECURITY_PRODUCT_STATE_SNOOZED, iwscapi/WSC_SECURITY_PRODUCT_STATE, iwscapi/WSC_SECURITY_PRODUCT_STATE_EXPIRED, iwscapi/WSC_SECURITY_PRODUCT_STATE_OFF, iwscapi/WSC_SECURITY_PRODUCT_STATE_ON, iwscapi/WSC_SECURITY_PRODUCT_STATE_SNOOZED, winprog.wsc_security_product_state
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wscapi.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSC_SECURITY_PRODUCT_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WSC_SECURITY_PRODUCT_STATE
 - iwscapi/WSC_SECURITY_PRODUCT_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Wscapi.lib
api_name:
 - WSC_SECURITY_PRODUCT_STATE
---

# WSC_SECURITY_PRODUCT_STATE enumeration


## -description

Defines the current state of the security product that is made available to Windows Security Center.

## -enum-fields

### -field WSC_SECURITY_PRODUCT_STATE_ON:0

The security product software is turned on and protecting the user.

### -field WSC_SECURITY_PRODUCT_STATE_OFF:1

The security product software is turned off and protection is disabled.

### -field WSC_SECURITY_PRODUCT_STATE_SNOOZED:2

The security product software is in the snoozed state, temporarily off,  and not actively protecting the computer.

### -field WSC_SECURITY_PRODUCT_STATE_EXPIRED:3

The security product software has expired and is no longer actively protecting the computer.

