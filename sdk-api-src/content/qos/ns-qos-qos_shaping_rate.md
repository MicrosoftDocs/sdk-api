---
UID: NS:qos._QOS_SHAPING_RATE
title: QOS_SHAPING_RATE (qos.h)
author: windows-sdk-content
description: The QOS object QOS_SHAPING_RATE specifies the uniform traffic shaping rate be applied to a given flow.
old-location: qos\qos_shaping_rate.htm
tech.root: QOS
ms.assetid: 2be833dc-d9e1-495d-831e-09c900c8adb2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPQOS_SHAPING_RATE, LPQOS_SHAPING_RATE, LPQOS_SHAPING_RATE structure pointer [QOS], QOS_SHAPING_RATE, QOS_SHAPING_RATE structure [QOS], _gqos_qos_shaping_rate, qos.qos_shaping_rate, qos/LPQOS_SHAPING_RATE, qos/QOS_SHAPING_RATE"
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos.h
api_name:
 - QOS_SHAPING_RATE
product: Windows
targetos: Windows
req.typenames: QOS_SHAPING_RATE, *LPQOS_SHAPING_RATE
req.redist: 
ms.custom: 19H1
---

# QOS_SHAPING_RATE structure


## -description


The QOS object 
<b>QOS_SHAPING_RATE</b> specifies the uniform traffic shaping rate be applied to a given flow.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_SHAPING_RATE</b>.


### -field ShapingRate

Unsigned 32-bit integer that specifies the uniform traffic shaping rate in bytes per second. 


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>
 

 

