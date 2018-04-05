---
UID: NS:qossp._PARAM_BUFFER
title: "_PARAM_BUFFER"
author: windows-driver-content
description: The PARAM_BUFFER structure describes the format of the parameter buffer that can be included in the CONTROL_SERVICE structure.
old-location: qos\param_buffer.htm
old-project: QOS
ms.assetid: b5078f3b-ab7f-4194-aed7-de5ebb4f7fb8
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPPARAM_BUFFER, *LPPARAM_BUFFER structure [QOS], PARAM_BUFFER, PARAM_BUFFER structure [QOS], _PARAM_BUFFER, qos.param_buffer, qossp/*LPPARAM_BUFFER, qossp/PARAM_BUFFER"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: PARAM_BUFFER, *LPPARAM_BUFFER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Qossp.h
api_name:
-	PARAM_BUFFER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _PARAM_BUFFER structure


## -description


The <b>PARAM_BUFFER</b> structure describes the format of the parameter buffer that can be included in the <a href="https://msdn.microsoft.com/604d7be8-955b-40a3-9cb4-6cbfbeeaa105">CONTROL_SERVICE</a> structure.


## -struct-fields




### -field ParameterId

Parameter ID, as defined by INTSERV.


### -field Length

Length of the entire <b>PARAM_BUFFER</b> structure.


### -field Buffer

Buffer containing the parameter.


## -see-also




<a href="https://msdn.microsoft.com/604d7be8-955b-40a3-9cb4-6cbfbeeaa105">CONTROL_SERVICE</a>
 

 

