---
UID: NS:qos._QOS_SHAPING_RATE
title: QOS_SHAPING_RATE (qos.h)
description: The QOS object QOS_SHAPING_RATE specifies the uniform traffic shaping rate be applied to a given flow.
helpviewer_keywords: ["*LPQOS_SHAPING_RATE","LPQOS_SHAPING_RATE","LPQOS_SHAPING_RATE structure pointer [QOS]","QOS_SHAPING_RATE","QOS_SHAPING_RATE structure [QOS]","_gqos_qos_shaping_rate","qos.qos_shaping_rate","qos/LPQOS_SHAPING_RATE","qos/QOS_SHAPING_RATE"]
old-location: qos\qos_shaping_rate.htm
tech.root: QOS
ms.assetid: 2be833dc-d9e1-495d-831e-09c900c8adb2
ms.date: 12/05/2018
ms.keywords: '*LPQOS_SHAPING_RATE, LPQOS_SHAPING_RATE, LPQOS_SHAPING_RATE structure pointer [QOS], QOS_SHAPING_RATE, QOS_SHAPING_RATE structure [QOS], _gqos_qos_shaping_rate, qos.qos_shaping_rate, qos/LPQOS_SHAPING_RATE, qos/QOS_SHAPING_RATE'
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
req.typenames: QOS_SHAPING_RATE, *LPQOS_SHAPING_RATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_SHAPING_RATE
 - qos/_QOS_SHAPING_RATE
 - LPQOS_SHAPING_RATE
 - qos/LPQOS_SHAPING_RATE
 - QOS_SHAPING_RATE
 - qos/QOS_SHAPING_RATE
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
 - QOS_SHAPING_RATE
---

# QOS_SHAPING_RATE structure


## -description

The QOS object 
<b>QOS_SHAPING_RATE</b> specifies the uniform traffic shaping rate be applied to a given flow.

## -struct-fields

### -field ObjectHdr

The QOS object 
<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_SHAPING_RATE</b>.

### -field ShapingRate

Unsigned 32-bit integer that specifies the uniform traffic shaping rate in bytes per second.

## -see-also

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>