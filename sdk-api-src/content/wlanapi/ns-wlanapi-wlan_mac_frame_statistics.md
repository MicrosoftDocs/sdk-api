---
UID: NS:wlanapi.WLAN_MAC_FRAME_STATISTICS
title: WLAN_MAC_FRAME_STATISTICS (wlanapi.h)
description: Contains information about sent and received MAC frames.
helpviewer_keywords: ["*PWLAN_MAC_FRAME_STATISTICS","PWLAN_MAC_FRAME_STATISTICS","PWLAN_MAC_FRAME_STATISTICS structure pointer [NativeWIFI]","WLAN_MAC_FRAME_STATISTICS","WLAN_MAC_FRAME_STATISTICS structure [NativeWIFI]","nwifi.wlan_mac_frame_statistics","wlanapi/PWLAN_MAC_FRAME_STATISTICS","wlanapi/WLAN_MAC_FRAME_STATISTICS"]
old-location: nwifi\wlan_mac_frame_statistics.htm
tech.root: nwifi
ms.assetid: b5bb4ec9-aeec-4a64-977d-e875c3835196
ms.date: 12/05/2018
ms.keywords: '*PWLAN_MAC_FRAME_STATISTICS, PWLAN_MAC_FRAME_STATISTICS, PWLAN_MAC_FRAME_STATISTICS structure pointer [NativeWIFI], WLAN_MAC_FRAME_STATISTICS, WLAN_MAC_FRAME_STATISTICS structure [NativeWIFI], nwifi.wlan_mac_frame_statistics, wlanapi/PWLAN_MAC_FRAME_STATISTICS, wlanapi/WLAN_MAC_FRAME_STATISTICS'
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
req.typenames: WLAN_MAC_FRAME_STATISTICS, *PWLAN_MAC_FRAME_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WLAN_MAC_FRAME_STATISTICS
 - wlanapi/WLAN_MAC_FRAME_STATISTICS
 - PWLAN_MAC_FRAME_STATISTICS
 - wlanapi/PWLAN_MAC_FRAME_STATISTICS
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
 - WLAN_MAC_FRAME_STATISTICS
---

# WLAN_MAC_FRAME_STATISTICS structure


## -description

The <b>WLAN_MAC_FRAME_STATISTICS</b> structure contains information about sent and received MAC frames.

## -struct-fields

### -field ullTransmittedFrameCount

Contains the number of successfully transmitted MSDU/MMPDUs.

### -field ullReceivedFrameCount

Contains the number of successfully received MSDU/MMPDUs.

### -field ullWEPExcludedCount

Contains the number of frames discarded due to having a "Protected" status indicated in the frame control field.

### -field ullTKIPLocalMICFailures

Contains the number of MIC failures encountered while checking the integrity of packets received from the AP or peer station.

### -field ullTKIPReplays

Contains the number of TKIP replay errors detected.

### -field ullTKIPICVErrorCount

Contains the number of TKIP protected packets that the NIC failed to decrypt.

### -field ullCCMPReplays

Contains the number of received unicast fragments discarded by the replay mechanism.

### -field ullCCMPDecryptErrors

Contains the number of received fragments discarded by the CCMP decryption algorithm.

### -field ullWEPUndecryptableCount

Contains the number of WEP protected packets received for which a decryption key was not available on the NIC.

### -field ullWEPICVErrorCount

Contains the number of WEP protected packets the NIC failed to decrypt.

### -field ullDecryptSuccessCount

Contains the number of encrypted packets that the NIC has successfully decrypted.

### -field ullDecryptFailureCount

Contains the number of encrypted packets that the NIC has failed to decrypt.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_statistics">WLAN_STATISTICS</a>