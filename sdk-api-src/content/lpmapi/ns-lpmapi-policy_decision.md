---
UID: NS:lpmapi.policy_decision
title: POLICY_DECISION (lpmapi.h)
description: The POLICY_DECISION structure contains RSVP policy decision information.
helpviewer_keywords: ["POLICY_DECISION","POLICY_DECISION structure [QOS]","lpmapi/POLICY_DECISION","qos.policy_decision"]
old-location: qos\policy_decision.htm
tech.root: QOS
ms.assetid: 6896031d-a8b4-46c5-bb52-61808bbb23f2
ms.date: 12/05/2018
ms.keywords: POLICY_DECISION, POLICY_DECISION structure [QOS], lpmapi/POLICY_DECISION, qos.policy_decision
req.header: lpmapi.h
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
req.typenames: POLICY_DECISION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - policy_decision
 - lpmapi/policy_decision
 - POLICY_DECISION
 - lpmapi/POLICY_DECISION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - POLICY_DECISION
---

# POLICY_DECISION structure


## -description

The 
<b>POLICY_DECISION</b> structure contains RSVP policy decision information.

## -struct-fields

### -field lpvResult

Local policy value.

### -field wPolicyErrCode

RSVP-defined error code.

### -field wPolicyErrValue

RSVP-defined error value.

## -see-also

<a href="/previous-versions/windows/desktop/qos/policy-elements">Policy Elements</a>