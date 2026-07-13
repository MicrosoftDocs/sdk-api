---
UID: NS:lpmapi.POLICY_DATA
title: POLICY_DATA (lpmapi.h)
description: The POLICY_DATA structure contains policy data for RSVP messages.
helpviewer_keywords: ["POLICY_DATA","POLICY_DATA structure [QOS]","lpmapi/POLICY_DATA","qos.policy_data"]
old-location: qos\policy_data.htm
tech.root: QOS
ms.assetid: 0e91b77c-e4dd-4e23-8af6-bf549168cfc5
ms.date: 12/05/2018
ms.keywords: POLICY_DATA, POLICY_DATA structure [QOS], lpmapi/POLICY_DATA, qos.policy_data
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
req.typenames: POLICY_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POLICY_DATA
 - lpmapi/POLICY_DATA
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
 - POLICY_DATA
---

# POLICY_DATA structure


## -description

The 
<b>POLICY_DATA</b> structure contains policy data for RSVP messages.

## -struct-fields

### -field PolicyObjHdr

Policy object header, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field usPeOffset

Offset to the beginning of Policy Elements from the beginning of Policy Data.

### -field usReserved

Reserved. Do not use.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

