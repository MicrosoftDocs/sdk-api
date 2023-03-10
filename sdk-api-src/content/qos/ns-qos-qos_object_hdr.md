---
UID: NS:qos.QOS_OBJECT_HDR
title: QOS_OBJECT_HDR (qos.h)
description: The QOS object QOS_OBJECT_HDR is attached to each QOS object. It specifies the object type and its length.
helpviewer_keywords: ["*LPQOS_OBJECT_HDR","LPQOS_OBJECT_HDR","LPQOS_OBJECT_HDR structure pointer [QOS]","QOS_OBJECT_DESTADDR","QOS_OBJECT_END_OF_LIST","QOS_OBJECT_HDR","QOS_OBJECT_HDR structure [QOS]","QOS_OBJECT_SD_MODE","QOS_OBJECT_SHAPING_RATE","RSVP_OBJECT_ADSPEC","RSVP_OBJECT_FILTERSPEC_LIST","RSVP_OBJECT_POLICY_INFO","RSVP_OBJECT_RESERVE_INFO","_gqos_qos_object_hdr","qos.qos_object_hdr","qos/LPQOS_OBJECT_HDR","qos/QOS_OBJECT_HDR"]
old-location: qos\qos_object_hdr.htm
tech.root: QOS
ms.assetid: a2021d70-e7ef-4c2a-8800-1a1d7540ce02
ms.date: 12/05/2018
ms.keywords: '*LPQOS_OBJECT_HDR, LPQOS_OBJECT_HDR, LPQOS_OBJECT_HDR structure pointer [QOS], QOS_OBJECT_DESTADDR, QOS_OBJECT_END_OF_LIST, QOS_OBJECT_HDR, QOS_OBJECT_HDR structure [QOS], QOS_OBJECT_SD_MODE, QOS_OBJECT_SHAPING_RATE, RSVP_OBJECT_ADSPEC, RSVP_OBJECT_FILTERSPEC_LIST, RSVP_OBJECT_POLICY_INFO, RSVP_OBJECT_RESERVE_INFO, _gqos_qos_object_hdr, qos.qos_object_hdr, qos/LPQOS_OBJECT_HDR, qos/QOS_OBJECT_HDR'
req.header: qos.h
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
req.typenames: QOS_OBJECT_HDR, *LPQOS_OBJECT_HDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPQOS_OBJECT_HDR
 - qos/LPQOS_OBJECT_HDR
 - QOS_OBJECT_HDR
 - qos/QOS_OBJECT_HDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos.h
api_name:
 - QOS_OBJECT_HDR
---

# QOS_OBJECT_HDR structure


## -description

The QOS object 
<b>QOS_OBJECT_HDR</b> is attached to each QOS object. It specifies the object type and its length.

## -struct-fields

### -field ObjectType

Specifies the type of object to which 
<b>QOS_OBJECT_HDR</b> is attached. The following values are valid for 
<b>QOS_OBJECT_HDR</b>: 




<a id="QOS_OBJECT_DESTADDR"></a>
<a id="qos_object_destaddr"></a>


#### QOS_OBJECT_DESTADDR

<a id="QOS_OBJECT_END_OF_LIST"></a>
<a id="qos_object_end_of_list"></a>


#### QOS_OBJECT_END_OF_LIST

<a id="QOS_OBJECT_SD_MODE"></a>
<a id="qos_object_sd_mode"></a>


#### QOS_OBJECT_SD_MODE

<a id="QOS_OBJECT_SHAPING_RATE"></a>
<a id="qos_object_shaping_rate"></a>


#### QOS_OBJECT_SHAPING_RATE

<a id="RSVP_OBJECT_ADSPEC"></a>
<a id="rsvp_object_adspec"></a>


#### RSVP_OBJECT_ADSPEC

<a id="RSVP_OBJECT_FILTERSPEC_LIST"></a>
<a id="rsvp_object_filterspec_list"></a>


#### RSVP_OBJECT_FILTERSPEC_LIST

<a id="RSVP_OBJECT_POLICY_INFO"></a>
<a id="rsvp_object_policy_info"></a>


#### RSVP_OBJECT_POLICY_INFO

<a id="RSVP_OBJECT_RESERVE_INFO"></a>
<a id="rsvp_object_reserve_info"></a>


#### RSVP_OBJECT_RESERVE_INFO

### -field ObjectLength

Specifies the length of the attached object, inclusive of QOS_OBJECT_HDR.

## -see-also

<a href="/windows/win32/api/winsock2/ns-winsock2-qos">QOS</a>

