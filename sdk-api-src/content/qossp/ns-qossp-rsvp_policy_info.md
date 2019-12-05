---
UID: NS:qossp._RSVP_POLICY_INFO
title: RSVP_POLICY_INFO (qossp.h)
description: The RSVP_POLICY_INFO structure stores undefined policy elements retrieved from RSVP.
old-location: qos\rsvp_policy_info.htm
tech.root: QOS
ms.assetid: 21ad9446-a22c-4c3f-911d-a263cb85078b
ms.date: 12/05/2018
ms.keywords: '*LPRSVP_POLICY_INFO, *LPRSVP_POLICY_INFO structure [QOS], RSVP_POLICY_INFO, RSVP_POLICY_INFO structure [QOS], qos.rsvp_policy_info, qossp/*LPRSVP_POLICY_INFO, qossp/RSVP_POLICY_INFO'
ms.topic: struct
f1_keywords:
- qossp/RSVP_POLICY_INFO
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Qossp.h
api_name:
- RSVP_POLICY_INFO
targetos: Windows
req.typenames: RSVP_POLICY_INFO, *LPRSVP_POLICY_INFO
req.redist: 
ms.custom: 19H1
---

# RSVP_POLICY_INFO structure


## -description


The <b>RSVP_POLICY_INFO</b> structure stores undefined policy elements retrieved from RSVP.


## -struct-fields




### -field ObjectHdr

QOS object header that specifies the size and length of the QOS object.


### -field NumPolicyElement

Number of policy elements in <b>PolicyElement</b>.


### -field PolicyElement

List of policy elements received, in the form of a <a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-rsvp_policy">RSVP_POLICY</a> structure.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qossp/ns-qossp-rsvp_policy">RSVP_POLICY</a>
 

 

