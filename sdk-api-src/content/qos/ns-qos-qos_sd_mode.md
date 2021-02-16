---
UID: NS:qos._QOS_SD_MODE
title: QOS_SD_MODE (qos.h)
description: The QOS object QOS_SD_MODE defines the behavior of the traffic control-packet shaper component.
helpviewer_keywords: ["*LPQOS_SD_MODE","LPQOS_SD_MODE","LPQOS_SD_MODE structure pointer [QOS]","QOS_SD_MODE","QOS_SD_MODE structure [QOS]","TC_NONCONF_BORROW","TC_NONCONF_DISCARD","TC_NONCONF_SHAPE","_gqos_qos_sd_mode","qos.qos_sd_mode","qos/LPQOS_SD_MODE","qos/QOS_SD_MODE"]
old-location: qos\qos_sd_mode.htm
tech.root: QOS
ms.assetid: a1ae9920-3e6f-4611-abce-905df7a516f5
ms.date: 12/05/2018
ms.keywords: '*LPQOS_SD_MODE, LPQOS_SD_MODE, LPQOS_SD_MODE structure pointer [QOS], QOS_SD_MODE, QOS_SD_MODE structure [QOS], TC_NONCONF_BORROW, TC_NONCONF_DISCARD, TC_NONCONF_SHAPE, _gqos_qos_sd_mode, qos.qos_sd_mode, qos/LPQOS_SD_MODE, qos/QOS_SD_MODE'
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
req.typenames: QOS_SD_MODE, *LPQOS_SD_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_SD_MODE
 - qos/_QOS_SD_MODE
 - LPQOS_SD_MODE
 - qos/LPQOS_SD_MODE
 - QOS_SD_MODE
 - qos/QOS_SD_MODE
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
 - QOS_SD_MODE
---

# QOS_SD_MODE structure


## -description

The QOS object 
<b>QOS_SD_MODE</b> defines the behavior of the traffic control-packet shaper component.

## -struct-fields

### -field ObjectHdr

The QOS object 
<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>. The object type for this QOS object should be 
<b>QOS_SD_MODE</b>.

### -field ShapeDiscardMode

Specifies the requested behavior of the packet shaper. Note that there are elements of packet handling within these predefined behaviors that depend on the flow settings specified within 
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>. 



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
<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a> is specified for this flow, packets that exceed the value of <b>TokenRate</b> will have their priority demoted to less than SERVICETYPE_BESTEFFORT, as defined in the <b>ServiceType</b> member of the 
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

<a href="/windows/desktop/api/qos/ns-qos-flowspec">FLOWSPEC</a>



<a href="/previous-versions/windows/desktop/api/qos/ns-qos-qos_object_hdr">QOS_OBJECT_HDR</a>