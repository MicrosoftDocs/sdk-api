---
UID: NS:qossp._RSVP_POLICY
title: RSVP_POLICY (qossp.h)
description: The RSVP_POLICY structure stores one or more undefined policy elements.
helpviewer_keywords: ["*LPRSVP_POLICY","*LPRSVP_POLICY structure [QOS]","RSVP_POLICY","RSVP_POLICY structure [QOS]","qos.rsvp_policy","qossp/*LPRSVP_POLICY","qossp/RSVP_POLICY"]
old-location: qos\rsvp_policy.htm
tech.root: QOS
ms.assetid: e23cd113-6fa1-479b-85c2-7690055e57e7
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_POLICY, *LPRSVP_POLICY structure [QOS], RSVP_POLICY, RSVP_POLICY structure [QOS], qos.rsvp_policy, qossp/*LPRSVP_POLICY, qossp/RSVP_POLICY'
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: RSVP_POLICY, *LPRSVP_POLICY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RSVP_POLICY
 - qossp/_RSVP_POLICY
 - LPRSVP_POLICY
 - qossp/LPRSVP_POLICY
 - RSVP_POLICY
 - qossp/RSVP_POLICY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qossp.h
api_name:
 - RSVP_POLICY
---

# RSVP_POLICY structure


## -description

The <b>RSVP_POLICY</b> structure stores one or more undefined policy elements.

## -struct-fields

### -field Len

Size of the entire element object, in bytes.

### -field Type

Type of RSVP policy element  in <b>Info</b>.

### -field Info

Policy data, expressed in UCHARs.

## -remarks

RSVP transports the data contained in an <b>RSVP_POLICY</b> structure on behalf of the Policy Control component.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-rsvp_policy_info">RSVP_POLICY_INFO</a>