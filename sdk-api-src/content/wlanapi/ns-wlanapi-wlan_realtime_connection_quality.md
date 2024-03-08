---
UID: NS:wlanapi._WLAN_REALTIME_CONNECTION_QUALITY
title: WLAN_REALTIME_CONNECTION_QUALITY
description: Represents the attributes that describe the quality of the connection on a given interface.
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
req.target-type: 
req.typenames: WLAN_REALTIME_CONNECTION_QUALITY, *PWLAN_REALTIME_CONNECTION_QUALITY
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
 - _WLAN_REALTIME_CONNECTION_QUALITY
 - PWLAN_REALTIME_CONNECTION_QUALITY
 - WLAN_REALTIME_CONNECTION_QUALITY
f1_keywords:
 - _WLAN_REALTIME_CONNECTION_QUALITY
 - wlanapi/_WLAN_REALTIME_CONNECTION_QUALITY
 - PWLAN_REALTIME_CONNECTION_QUALITY
 - wlanapi/PWLAN_REALTIME_CONNECTION_QUALITY
 - WLAN_REALTIME_CONNECTION_QUALITY
 - wlanapi/WLAN_REALTIME_CONNECTION_QUALITY
dev_langs:
 - c++
helpviewer_keywords:
 - _WLAN_REALTIME_CONNECTION_QUALITY
prerelease: true
---

## -description

Represents the attributes that describe the quality of the connection on a given interface.

## -struct-fields

### -field dot11PhyType

TBD

### -field ulLinkQuality

TBD

### -field ulRxRate

TBD

### -field ulTxRate

TBD

### -field bIsMLOConnection

TBD

### -field ulNumLinks

TBD

### -field ulLinkInfoOffset

TBD

## -remarks

## Examples

```cppwinrt
DWORD IsWLANLinkSpeedSufficient(
    GUID* interfaceGuid,
    const ULONG minRequiredLinkQuality,
    const ULONG requiredRxRate,
    const ULONG requiredTxRate,
    bool* isSufficient)
{
    wil::unique_wlan_handle clientHandle;
    DWORD maxClientVersion = 2;
    DWORD currentClientVersion = 0;
    DWORD result = WlanOpenHandle(maxClientVersion, nullptr, &currentClientVersion, &clientHandle);
    if (result != ERROR_SUCCESS) 
    {
        wprintf(L"WlanOpenHandle failed with error: %u\n", result);
        return result;
    }

    DWORD connectionQualitySize = 0;
    wil::unique_wlan_ptr<WLAN_REALTIME_CONNECTION_QUALITY> connectionQuality;
    result = WlanQueryInterface(
        clientHandle.get(), 
        interfaceGuid,
        wlan_intf_opcode_realtime_connection_quality,
        nullptr,
        &connectionQualitySize,
        wil::out_param_ptr<void**>(connectionQuality),
        nullptr);
    if (result != ERROR_SUCCESS) 
    {
        wprintf(L"WlanQueryInterface failed with error: %u\n", result);
        return result;
    }

    if (connectionQuality->ulLinkQuality < minRequiredLinkQuality || 
        connectionQuality->ulRxRate < requiredRxRate ||
        connectionQuality->ulTxRate < requiredTxRate)
    {
        *isSufficient = false;
    }
    else
    {
        *isSufficient = true;
    }
    return ERROR_SUCCESS;
}

DWORD GetCenterChannelFrequencyOfLinkWithBestRSSI(GUID* interfaceGuid, ULONG* channelFrequency)
{
    wil::unique_wlan_handle clientHandle;
    DWORD maxClientVersion = 2;
    DWORD currentClientVersion = 0;
    DWORD result = WlanOpenHandle(maxClientVersion, nullptr, &currentClientVersion, &clientHandle);
    if (result != ERROR_SUCCESS) 
    {
        wprintf(L"WlanOpenHandle failed with error: %u\n", result);
        return result;
    }

    DWORD connectionQualitySize = 0;
    wil::unique_wlan_ptr<WLAN_REALTIME_CONNECTION_QUALITY> connectionQuality;
    result = WlanQueryInterface(
        clientHandle.get(), 
        interfaceGuid,
        wlan_intf_opcode_realtime_connection_quality,
        nullptr,
        &connectionQualitySize,
        wil::out_param_ptr<void**>(connectionQuality),
        nullptr);
    if (result != ERROR_SUCCESS) 
    {
        wprintf(L"WlanQueryInterface failed with error: %u\n", result);
        return result;
    }

    auto linkWithBestRssi = std::min_element(
        connectionQuality->linksInfo,
        connectionQuality->linksInfo + connectionQuality->ulNumLinks,
        [](const WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO& lhs, const WLAN_REALTIME_CONNECTION_QUALITY_LINK_INFO& rhs) {
            return lhs.lRssi > rhs.lRssi; // `Greater than` because RSSI is negative.
        });

    *channelFrequency = linkWithBestRssi->ulChannelCenterFrequencyMhz;
    return ERROR_SUCCESS;
}
```

## -see-also
