---
UID: NE:iwscapi.WSC_SECURITY_PRODUCT_STATE
title: WSC_SECURITY_PRODUCT_STATE
author: windows-driver-content
description: Defines the current state of the security product that is made available to Windows Security Center.
old-location: winprog\wsc_security_product_state.htm
old-project: DevNotes
ms.assetid: 2783795B-4A7A-4033-A9EE-9B4CEF2E61B9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: WSC_SECURITY_PRODUCT_STATE, WSC_SECURITY_PRODUCT_STATE enumeration [Windows API], WSC_SECURITY_PRODUCT_STATE_EXPIRED, WSC_SECURITY_PRODUCT_STATE_OFF, WSC_SECURITY_PRODUCT_STATE_ON, WSC_SECURITY_PRODUCT_STATE_SNOOZED, iwscapi/WSC_SECURITY_PRODUCT_STATE, iwscapi/WSC_SECURITY_PRODUCT_STATE_EXPIRED, iwscapi/WSC_SECURITY_PRODUCT_STATE_OFF, iwscapi/WSC_SECURITY_PRODUCT_STATE_ON, iwscapi/WSC_SECURITY_PRODUCT_STATE_SNOOZED, winprog.wsc_security_product_state
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: WSC_SECURITY_PRODUCT_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	LibDef
api_location:
-	Wscapi.lib
api_name:
-	WSC_SECURITY_PRODUCT_STATE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# WSC_SECURITY_PRODUCT_STATE enumeration


## -description


Defines the current state of the security product that is made available to Windows Security Center. 


## -enum-fields




### -field WSC_SECURITY_PRODUCT_STATE_ON

The security product software is turned on and protecting the user.


### -field WSC_SECURITY_PRODUCT_STATE_OFF

The security product software is turned off and protection is disabled.


### -field WSC_SECURITY_PRODUCT_STATE_SNOOZED

The security product software is in the snoozed state, temporarily off,  and not actively protecting the computer.


### -field WSC_SECURITY_PRODUCT_STATE_EXPIRED

The security product software has expired and is no longer actively protecting the computer.

