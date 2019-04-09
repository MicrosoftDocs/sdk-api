---
UID: NS:qossp._RSVP_POLICY
title: RSVP_POLICY (qossp.h)
author: windows-sdk-content
description: The RSVP_POLICY structure stores one or more undefined policy elements.
old-location: qos\rsvp_policy.htm
tech.root: QOS
ms.assetid: e23cd113-6fa1-479b-85c2-7690055e57e7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPRSVP_POLICY, *LPRSVP_POLICY structure [QOS], RSVP_POLICY, RSVP_POLICY structure [QOS], qos.rsvp_policy, qossp/*LPRSVP_POLICY, qossp/RSVP_POLICY"
ms.topic: struct
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
 - RSVP_POLICY
product: Windows
targetos: Windows
req.typenames: RSVP_POLICY, *LPRSVP_POLICY
req.redist: 
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




<a href="https://msdn.microsoft.com/21ad9446-a22c-4c3f-911d-a263cb85078b">RSVP_POLICY_INFO</a>
 

 

