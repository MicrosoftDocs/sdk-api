---
UID: NE:tapi3if.QOS_SERVICE_LEVEL
title: QOS_SERVICE_LEVEL (tapi3if.h)
description: The QOS_SERVICE_LEVEL enum is used by the ITBasicCallControl::SetQOS method to indicate quality of service requirements for a call.
helpviewer_keywords: ["QOS_SERVICE_LEVEL","QOS_SERVICE_LEVEL enumeration [TAPI 2.2]","QSL_BEST_EFFORT","QSL_IF_AVAILABLE","QSL_NEEDED","_tapi3_qos_service_level","tapi3.qos_service_level","tapi3if/QOS_SERVICE_LEVEL","tapi3if/QSL_BEST_EFFORT","tapi3if/QSL_IF_AVAILABLE","tapi3if/QSL_NEEDED"]
old-location: tapi3\qos_service_level.htm
tech.root: tapi3
ms.assetid: 8b0a93ab-6445-4c60-9d27-552c355c1355
ms.date: 12/05/2018
ms.keywords: QOS_SERVICE_LEVEL, QOS_SERVICE_LEVEL enumeration [TAPI 2.2], QSL_BEST_EFFORT, QSL_IF_AVAILABLE, QSL_NEEDED, _tapi3_qos_service_level, tapi3.qos_service_level, tapi3if/QOS_SERVICE_LEVEL, tapi3if/QSL_BEST_EFFORT, tapi3if/QSL_IF_AVAILABLE, tapi3if/QSL_NEEDED
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: QOS_SERVICE_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QOS_SERVICE_LEVEL
 - tapi3if/QOS_SERVICE_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - QOS_SERVICE_LEVEL
---

# QOS_SERVICE_LEVEL enumeration


## -description

The 
<b>QOS_SERVICE_LEVEL</b> enum is used by the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos">ITBasicCallControl::SetQOS</a> method to indicate quality of service requirements for a call.

## -enum-fields

### -field QSL_NEEDED:1

Quality of service level required.

### -field QSL_IF_AVAILABLE:2

Quality of service level desired if available.

### -field QSL_BEST_EFFORT:3

Quality of service level desired is "best effort."

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos">ITBasicCallControl::SetQOS</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>
