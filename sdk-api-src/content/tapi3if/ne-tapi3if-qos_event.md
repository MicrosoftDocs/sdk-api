---
UID: NE:tapi3if.QOS_EVENT
title: QOS_EVENT (tapi3if.h)
description: The QOS_EVENT enum describes quality of service (QOS) events. The ITQOSEvent::get_Event method returns a member of this enum to indicate the type of QOS event that occurred.
helpviewer_keywords: ["QE_ADMISSIONFAILURE","QE_GENERICERROR","QE_NOQOS","QE_POLICYFAILURE","QOS_EVENT","QOS_EVENT enumeration [TAPI 2.2]","_tapi3_qos_event","tapi3.qos_event","tapi3if/QE_ADMISSIONFAILURE","tapi3if/QE_GENERICERROR","tapi3if/QE_NOQOS","tapi3if/QE_POLICYFAILURE","tapi3if/QOS_EVENT"]
old-location: tapi3\qos_event.htm
tech.root: tapi3
ms.assetid: 8bf4bfdc-6327-497d-9d19-4771d47982bb
ms.date: 12/05/2018
ms.keywords: QE_ADMISSIONFAILURE, QE_GENERICERROR, QE_NOQOS, QE_POLICYFAILURE, QOS_EVENT, QOS_EVENT enumeration [TAPI 2.2], _tapi3_qos_event, tapi3.qos_event, tapi3if/QE_ADMISSIONFAILURE, tapi3if/QE_GENERICERROR, tapi3if/QE_NOQOS, tapi3if/QE_POLICYFAILURE, tapi3if/QOS_EVENT
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
req.typenames: QOS_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - QOS_EVENT
 - tapi3if/QOS_EVENT
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
 - QOS_EVENT
---

# QOS_EVENT enumeration


## -description

The 
<b>QOS_EVENT</b> enum describes quality of service (QOS) events. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_event">ITQOSEvent::get_Event</a> method returns a member of this enum to indicate the type of QOS event that occurred.

## -enum-fields

### -field QE_NOQOS:1

QOS is not available.

### -field QE_ADMISSIONFAILURE:2

The QOS request could not be met.

### -field QE_POLICYFAILURE:3

The type of QOS requested is not supported.

### -field QE_GENERICERROR:4

Unspecified QOS error.

### -field QE_LASTITEM

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos">ITBasicCallControl::SetQOS</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itqosevent-get_event">ITQOSEvent::get_Event</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-qos_service_level">QOS_SERVICE_LEVEL</a>
