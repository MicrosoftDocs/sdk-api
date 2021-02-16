---
UID: NS:qossp._PARAM_BUFFER
title: PARAM_BUFFER (qossp.h)
description: The PARAM_BUFFER structure describes the format of the parameter buffer that can be included in the CONTROL_SERVICE structure.
helpviewer_keywords: ["*LPPARAM_BUFFER","*LPPARAM_BUFFER structure [QOS]","PARAM_BUFFER","PARAM_BUFFER structure [QOS]","qos.param_buffer","qossp/*LPPARAM_BUFFER","qossp/PARAM_BUFFER"]
old-location: qos\param_buffer.htm
tech.root: QOS
ms.assetid: b5078f3b-ab7f-4194-aed7-de5ebb4f7fb8
ms.date: 12/05/2018
ms.keywords: '*LPPARAM_BUFFER, *LPPARAM_BUFFER structure [QOS], PARAM_BUFFER, PARAM_BUFFER structure [QOS], qos.param_buffer, qossp/*LPPARAM_BUFFER, qossp/PARAM_BUFFER'
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
req.typenames: PARAM_BUFFER, *LPPARAM_BUFFER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PARAM_BUFFER
 - qossp/_PARAM_BUFFER
 - LPPARAM_BUFFER
 - qossp/LPPARAM_BUFFER
 - PARAM_BUFFER
 - qossp/PARAM_BUFFER
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
 - PARAM_BUFFER
---

# PARAM_BUFFER structure


## -description

The <b>PARAM_BUFFER</b> structure describes the format of the parameter buffer that can be included in the <a href="/windows/desktop/api/qossp/ns-qossp-control_service">CONTROL_SERVICE</a> structure.

## -struct-fields

### -field ParameterId

Parameter ID, as defined by INTSERV.

### -field Length

Length of the entire <b>PARAM_BUFFER</b> structure.

### -field Buffer

Buffer containing the parameter.

## -see-also

<a href="/windows/desktop/api/qossp/ns-qossp-control_service">CONTROL_SERVICE</a>