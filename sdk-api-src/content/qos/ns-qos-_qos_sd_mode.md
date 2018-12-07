---
UID: NS:qos._QOS_SD_MODE
title: "_QOS_SD_MODE"
author: windows-sdk-content
description: The QOS object QOS_SD_MODE defines the behavior of the traffic control-packet shaper component.
old-location: qos\qos_sd_mode.htm
tech.root: QOS
ms.assetid: a1ae9920-3e6f-4611-abce-905df7a516f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPQOS_SD_MODE, LPQOS_SD_MODE, LPQOS_SD_MODE structure pointer [QOS], QOS_SD_MODE, QOS_SD_MODE structure [QOS], TC_NONCONF_BORROW, TC_NONCONF_DISCARD, TC_NONCONF_SHAPE, _QOS_SD_MODE, _gqos_qos_sd_mode, qos.qos_sd_mode, qos/LPQOS_SD_MODE, qos/QOS_SD_MODE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - QOS_SD_MODE
product: Windows
targetos: Windows
req.typenames: QOS_SD_MODE, *LPQOS_SD_MODE
req.redist: 
---

# _QOS_SD_MODE structure


## -description


The QOS object 
<b>QOS_SD_MODE</b> defines the behavior of the traffic control-packet shaper component.


## -struct-fields




### -field ObjectHdr

The QOS object 
<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_SD_MODE</b>.


### -field ShapeDiscardMode

Specifies the requested behavior of the packet shaper. Note that there are elements of packet handling within these predefined behaviors that depend on the flow settings specified within 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TC_NONCONF_BORROW"></a><a id="tc_nonconf_borrow"></a><dl>
<dt><b>TC_NONCONF_BORROW</b></dt>
</dl>
</td>
<td width="60%">
This mode is currently only available to the TC API. It is not available to users of the QOS API. 




Instructs the packet shaper to borrow remaining available resources after all higher priority flows have been serviced. If the <b>TokenRate</b> member of 
<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> is specified for this flow, packets that exceed the value of <b>TokenRate</b> will have their priority demoted to less than SERVICETYPE_BESTEFFORT, as defined in the <b>ServiceType</b> member of the 
<b>FLOWSPEC</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TC_NONCONF_SHAPE"></a><a id="tc_nonconf_shape"></a><dl>
<dt><b>TC_NONCONF_SHAPE</b></dt>
</dl>
</td>
<td width="60%">
Instructs the packet shaper to retain packets until network resources are available to the flow in sufficient quantity to make such packets conforming. (For example, a 100K packet will be retained in the packet shaper until 100K worth of credit is accrued for the flow, allowing the packet to be transmitted as conforming). Note that TokenRate must be specified if using TC_NONCONF_SHAPE.

</td>
</tr>
<tr>
<td width="40%"><a id="TC_NONCONF_DISCARD"></a><a id="tc_nonconf_discard"></a><dl>
<dt><b>TC_NONCONF_DISCARD</b></dt>
</dl>
</td>
<td width="60%">
Instructs the packet shaper to discard all nonconforming packets. TC_NONCONF_DISCARD should be used with care.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/a2021d70-e7ef-4c2a-8800-1a1d7540ce02">QOS_OBJECT_HDR</a>
 

 

