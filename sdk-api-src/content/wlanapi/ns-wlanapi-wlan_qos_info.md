---
UID: NS:wlanapi._WLAN_QOS_INFO
title: WLAN_QOS_INFO
description: Represents information about the four features outlined in the WFA's Wi-Fi QoS Management Specification, and defined in the 802.11 spec.
tech.root: nwifi
ms.date: 03/05/2024
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: wlanapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: Windows
req.typenames: WLAN_QOS_INFO, *PWLAN_QOS_INFO
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - _WLAN_QOS_INFO
 - PWLAN_QOS_INFO
 - WLAN_QOS_INFO
f1_keywords:
 - _WLAN_QOS_INFO
 - wlanapi/_WLAN_QOS_INFO
 - PWLAN_QOS_INFO
 - wlanapi/PWLAN_QOS_INFO
 - WLAN_QOS_INFO
 - wlanapi/WLAN_QOS_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_QOS_INFO
prerelease: true
---

## -description

Represents information about the four features outlined in the [WFA's Wi-Fi QoS Management Specification](https://www.wi-fi.org/news-events/newsroom/wi-fi-alliance-improves-quality-of-service-for-real-time-wi-fi-applications), and defined in the [802.11 spec](https://standards.ieee.org/ieee/802.11/7028/).

## -struct-fields

### -field interfaceCapabilities

Type: **[WLAN_QOS_CAPABILITIES](./ns-wlanapi-wlan_qos_capabilities.md)**

The QoS capabilities of the interface.

### -field bConnected

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

Represents whether or not there's an established connection. If `TRUE`, then *connectionQoSInfo* holds QoS information about the current connection. Otherwise, *connectionoQoSInfo* will be zeroed.

### -field connectionQoSInfo

Type: **[WLAN_CONNECTION_QOS_INFO](./ns-wlanapi-wlan_connection_qos_info.md)**

Information about the QoS features (outlined by the WFA Wi-Fi QoS Management Specification) pertaining to the current connection. This structure contains relevant information only if *bConnected* is `TRUE`; otherwise it is all zeros, and you should ignore it.

## -remarks

## Examples

```cppwinrt
void DisplayQoSInfo(GUID interfaceGuid)
{
    wil::unique_wlan_handle clientHandle;
    const DWORD maxClientVersion = 2;
    DWORD currentClientVersion = 0;
    DWORD status = WlanOpenHandle(maxClientVersion, nullptr, &currentClientVersion, &clientHandle);
    if (status != ERROR_SUCCESS) 
    {
        wprintf(L"WlanOpenHandle failed with error: %u\n", status);
        return;
    }

    wil::unique_wlan_ptr<WLAN_QOS_INFO> qosInfo;
    DWORD dataSize;
    status = WlanQueryInterface(clientHandle.get(), &interfaceGuid, wlan_intf_opcode_qos_info, nullptr, &dataSize, wil::out_param_ptr<void **>(qosInfo), nullptr);
    if (status != ERROR_SUCCESS)
    {
        wprintf(L"WlanQueryInterface failed with error %u\n", status);
        return;
    }

    wprintf(
        L"Interface QoS Capabilities: MSCS Supported = %u, DSCP To UP Mapping Supported = %u, SCS Supported = %u, DSCP Policy Supported = %u\n",
        qosInfo->interfaceCapabilities.bMSCSSupported,
        qosInfo->interfaceCapabilities.bDSCPToUPMappingSupported,
        qosInfo->interfaceCapabilities.bSCSSupported,
        qosInfo->interfaceCapabilities.bDSCPPolicySupported);

    if (!qosInfo->bConnected)
    {
        // Not connected, so the data that follows in connectionQoSInfo is meaningless.
        return;
    }

    const auto& connectionQoSInfo = qosInfo->connectionQoSInfo;
    wprintf(
        L"AP QoS Capabilities: MSCS Supported = %u, DSCP To UP Mapping Supported = %u, SCS Supported = %u, DSCP Policy Supported = %u\n",
        connectionQoSInfo.peerCapabilities.bMSCSSupported,
        connectionQoSInfo.peerCapabilities.bDSCPToUPMappingSupported,
        connectionQoSInfo.peerCapabilities.bSCSSupported,
        connectionQoSInfo.peerCapabilities.bDSCPPolicySupported);

    wprintf(
        L"Connection QoS Info:\n\tMSCS Configured = %u\n\tDSCP To UP Mapping Configured = %u\n\tNumber of SCS Streams = %u\n\tNumber of DSCP Policies = %u\n",
        connectionQoSInfo.bMSCSConfigured,
        connectionQoSInfo.bDSCPToUPMappingConfigured,
        connectionQoSInfo.ulNumConfiguredSCSStreams,
        connectionQoSInfo.ulNumConfiguredDSCPPolicies);
}
```

## -see-also
