---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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

Contains the number of MSDU/MMPDUs successfully received only because promicscuous mode is enabled.


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




<a href="https://msdn.microsoft.com/d66d89f1-bb12-4c2e-8c7a-a4eba008955d">WLAN_STATISTICS</a>
 

 

