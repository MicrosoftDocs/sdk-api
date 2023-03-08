---
UID: NS:wlanapi.WLAN_PHY_FRAME_STATISTICS
title: WLAN_PHY_FRAME_STATISTICS (wlanapi.h)
description: Contains information about sent and received PHY frames.
helpviewer_keywords: ["*PWLAN_PHY_FRAME_STATISTICS","PWLAN_PHY_FRAME_STATISTICS","PWLAN_PHY_FRAME_STATISTICS structure pointer [NativeWIFI]","WLAN_PHY_FRAME_STATISTICS","WLAN_PHY_FRAME_STATISTICS structure [NativeWIFI]","nwifi.wlan_phy_frame_statistics","wlanapi/PWLAN_PHY_FRAME_STATISTICS","wlanapi/WLAN_PHY_FRAME_STATISTICS"]
old-location: nwifi\wlan_phy_frame_statistics.htm
tech.root: nwifi
ms.assetid: c675a3cd-bbe5-473e-b734-12e74fd19a50
ms.date: 12/05/2018
ms.keywords: '*PWLAN_PHY_FRAME_STATISTICS, PWLAN_PHY_FRAME_STATISTICS, PWLAN_PHY_FRAME_STATISTICS structure pointer [NativeWIFI], WLAN_PHY_FRAME_STATISTICS, WLAN_PHY_FRAME_STATISTICS structure [NativeWIFI], nwifi.wlan_phy_frame_statistics, wlanapi/PWLAN_PHY_FRAME_STATISTICS, wlanapi/WLAN_PHY_FRAME_STATISTICS'
req.header: wlanapi.h
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
req.typenames: WLAN_PHY_FRAME_STATISTICS, *PWLAN_PHY_FRAME_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WLAN_PHY_FRAME_STATISTICS
 - wlanapi/WLAN_PHY_FRAME_STATISTICS
 - PWLAN_PHY_FRAME_STATISTICS
 - wlanapi/PWLAN_PHY_FRAME_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_PHY_FRAME_STATISTICS
---

# WLAN_PHY_FRAME_STATISTICS structure


## -description

The <b>WLAN_PHY_FRAME_STATISTICS</b> structure contains information about sent and received PHY frames

## -struct-fields

### -field ullTransmittedFrameCount

Contains the number of successfully transmitted MSDU/MMPDUs.

### -field ullMulticastTransmittedFrameCount

Contains the number of successfully transmitted MSDU/MMPDUs in which the multicast bit is set as the destination MAC address.

### -field ullFailedCount

Contains the number of MSDU/MMPDUs transmission failures due to the number of transmit attempts exceeding the retry limit.

### -field ullRetryCount

Contains the number of MSDU/MMPDUs successfully transmitted after one or more retransmissions.

### -field ullMultipleRetryCount

Contains the number of MSDU/MMPDUs successfully transmitted after more than one retransmission.

### -field ullMaxTXLifetimeExceededCount

Contains the number of fragmented MSDU/MMPDUs that failed to send due to timeout.

### -field ullTransmittedFragmentCount

Contains the number of MPDUs with an individual address in the address 1 field and MPDUs that have a multicast address  with types Data or Management.

### -field ullRTSSuccessCount

Contains the number of times a CTS has been received in response to an RTS.

### -field ullRTSFailureCount

Contains the number of times a CTS has not been received in response to an RTS.

### -field ullACKFailureCount

Contains the number of times an expected ACK has not been received.

### -field ullReceivedFrameCount

Contains the number of MSDU/MMPDUs successfully received.

### -field ullMulticastReceivedFrameCount

Contains the number of successfully received MSDU/MMPDUs with the multicast bit set in the MAC address.

### -field ullPromiscuousReceivedFrameCount

Contains the number of MSDU/MMPDUs successfully received only because promiscuous mode is enabled.

### -field ullMaxRXLifetimeExceededCount

Contains the number of fragmented MSDU/MMPDUs dropped due to timeout.

### -field ullFrameDuplicateCount

Contains the number of frames received that the Sequence Control field indicates as a duplicate.

### -field ullReceivedFragmentCount

Contains the number of successfully received Data or Management MPDUs.

### -field ullPromiscuousReceivedFragmentCount

Contains the number of MPDUs successfully received only because promiscuous mode is enabled.

### -field ullFCSErrorCount

Contains the number of times an FCS error has been detected in a received MPDU.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_statistics">WLAN_STATISTICS</a>