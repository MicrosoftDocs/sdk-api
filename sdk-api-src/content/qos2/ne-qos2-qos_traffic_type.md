---
UID: NE:qos2._QOS_TRAFFIC_TYPE
title: QOS_TRAFFIC_TYPE (qos2.h)
description: The QOS_TRAFFIC_TYPE enumeration defines the various traffic types. Each flow has a single traffic type. This allows the QOS subsystem to apply user-specified policies to each type.
helpviewer_keywords: ["*PQOS_TRAFFIC_TYPE","PQOS_TRAFFIC_TYPE","PQOS_TRAFFIC_TYPE enumeration pointer [QOS]","QOSTrafficTypeAudioVideo","QOSTrafficTypeBackground","QOSTrafficTypeBestEffort","QOSTrafficTypeControl","QOSTrafficTypeExcellentEffort","QOSTrafficTypeVoice","QOS_TRAFFIC_TYPE","QOS_TRAFFIC_TYPE enumeration [QOS]","qos.qos_traffic_type","qos2/PQOS_TRAFFIC_TYPE","qos2/QOSTrafficTypeAudioVideo","qos2/QOSTrafficTypeBackground","qos2/QOSTrafficTypeBestEffort","qos2/QOSTrafficTypeControl","qos2/QOSTrafficTypeExcellentEffort","qos2/QOSTrafficTypeVoice","qos2/QOS_TRAFFIC_TYPE"]
old-location: qos\qos_traffic_type.htm
tech.root: QOS
ms.assetid: 89145c7f-0b67-4eff-b462-049b047e6602
ms.date: 12/05/2018
ms.keywords: '*PQOS_TRAFFIC_TYPE, PQOS_TRAFFIC_TYPE, PQOS_TRAFFIC_TYPE enumeration pointer [QOS], QOSTrafficTypeAudioVideo, QOSTrafficTypeBackground, QOSTrafficTypeBestEffort, QOSTrafficTypeControl, QOSTrafficTypeExcellentEffort, QOSTrafficTypeVoice, QOS_TRAFFIC_TYPE, QOS_TRAFFIC_TYPE enumeration [QOS], qos.qos_traffic_type, qos2/PQOS_TRAFFIC_TYPE, qos2/QOSTrafficTypeAudioVideo, qos2/QOSTrafficTypeBackground, qos2/QOSTrafficTypeBestEffort, qos2/QOSTrafficTypeControl, qos2/QOSTrafficTypeExcellentEffort, qos2/QOSTrafficTypeVoice, qos2/QOS_TRAFFIC_TYPE'
req.header: qos2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: QOS_TRAFFIC_TYPE, *PQOS_TRAFFIC_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QOS_TRAFFIC_TYPE
 - qos2/_QOS_TRAFFIC_TYPE
 - PQOS_TRAFFIC_TYPE
 - qos2/PQOS_TRAFFIC_TYPE
 - QOS_TRAFFIC_TYPE
 - qos2/QOS_TRAFFIC_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Qos2.h
api_name:
 - QOS_TRAFFIC_TYPE
---

# QOS_TRAFFIC_TYPE enumeration


## -description

The <b>QOS_TRAFFIC_TYPE</b> enumeration defines the various traffic types.  Each flow has a single traffic type.  This allows the QOS subsystem to apply user-specified policies to each type.

## -enum-fields

### -field QOSTrafficTypeBestEffort:0

Flow traffic has the same network priority as regular traffic not associated with QOS.

This traffic type is the same as not specifying priority, and as a result,  the DSCP mark and 802.1p tag are not added to sent traffic.

### -field QOSTrafficTypeBackground:1

Flow traffic has a network priority lower than that of <b>QOSTrafficTypeBestEffort</b>.  This traffic type could be used for traffic of an application doing data backup.

Sent traffic will contain a DSCP mark with a value of 0x08 and an 802.1p tag with a value of 2.

### -field QOSTrafficTypeExcellentEffort:2

Flow traffic has a network priority higher than <b>QOSTrafficTypeBestEffort</b>, yet lower than <b>QOSTrafficTypeAudioVideo</b>.  This traffic type should be used for data traffic that is more important than normal end-user scenarios, such as email.

Sent traffic will contain a DSCP mark with value of 0x28 and 802.1p tag with a value of 5.

### -field QOSTrafficTypeAudioVideo:3

Flow traffic has a network priority higher than <b>QOSTrafficTypeExcellentEffort</b>, yet lower than <b>QOSTrafficTypeVoice</b>.  This traffic type should be used for A/V streaming scenarios such as MPEG2 streaming.

Sent traffic will contain a DSCP mark with a value of 0x28 and an 802.1p tag with a value of 5.

### -field QOSTrafficTypeVoice:4

Flow traffic has a network priority higher than <b>QOSTrafficTypeAudioVideo</b>, yet lower than <b>QOSTrafficTypeControl</b>.  This traffic type should be used for realtime voice streams such as VOIP.

Sent traffic will contain a DSCP mark with a value of 0x38 and an 802.1p tag with a value of 7.

### -field QOSTrafficTypeControl:5

Flow traffic has the highest network priority.  This traffic type should only be used for the most critical of data.  For example, it may be used for data carrying user inputs.

Sent traffic will contain a DSCP mark with a value of 0x38 and an 802.1p tag with a value of 7.

## -remarks

802.1p tags are  added to sent traffic only when the following conditions are met:<ul>
<li>
<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosaddsockettoflow">QOSAddSocketToFlow</a> is called without the QOS_NON_ADAPTIVE_FLOW flag</li>
<li> The destination host is on the local link and not across a router</li>
<li>The qWAVE subsystem has determined that 802.1p tagged packets are not discarded by a network element on the end-to-end path
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qosaddsockettoflow">QOSAddSocketToFlow</a>



<a href="/previous-versions/windows/desktop/api/qos2/nf-qos2-qossetflow">QOSSetFlow</a>



<a href="/previous-versions/windows/desktop/qos/quality-windows-audio-video-experience--qwave-">Quality Windows Audio/Video Experience (qWAVE)</a>
