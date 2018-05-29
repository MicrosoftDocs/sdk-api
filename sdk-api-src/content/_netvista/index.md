---
UID: TP:netvista
ms.assetid: 81753000-e53e-3c99-bde3-5c662c944380
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Network Drivers, Windows Vista and Later



Overview of the Network Drivers, Windows Vista and Later technology.

To develop Network Drivers, Windows Vista and Later, you need these headers:

 * [fwpstypes.h](..\fwpstypes\index.md)
 * [l2cmn.h](..\l2cmn\index.md)
 * [ndkinfo.h](..\ndkinfo\index.md)

For the programming guide, see [Network Drivers, Windows Vista and Later](/windows/desktop/netvista).

## Structures

| Title   | Description   |
| ---- |:---- |
| [FWPS_ACTION0_ structure](..\fwpstypes\ns-fwpstypes-fwps_action0_.md) | The FWPS_ACTION0 structure specifies the run-time action that the filter engine takes if all of the filter's filtering conditions are true.Note  FWPS_ACTION0 is a specific version of FWPS_ACTION. |
| [FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0_ structure](..\fwpstypes\ns-fwpstypes-fwps_ale_endpoint_enum_template0_.md) | The FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 structure specifies a template for application layer enforcement (ALE) endpoints to be enumerated.Note  FWPS_ALE_ENDPOINT_ENUM_TEMPLATE0 is a specific version of FWPS_ALE_ENDPOINT_ENUM_TEMPLATE. |
| [FWPS_ALE_ENDPOINT_PROPERTIES0_ structure](..\fwpstypes\ns-fwpstypes-fwps_ale_endpoint_properties0_.md) | The FWPS_ALE_ENDPOINT_PROPERTIES0 structure specifies the properties of an application layer enforcement (ALE) endpoint.Note  FWPS_ALE_ENDPOINT_PROPERTIES0 is a specific version of FWPS_ALE_ENDPOINT_PROPERTIES. |
| [FWPS_CLASSIFY_OUT0_ structure](..\fwpstypes\ns-fwpstypes-fwps_classify_out0_.md) | The FWPS_CLASSIFY_OUT0 structure defines the data that is returned to the caller of a callout's classifyFn callout function.Note  FWPS_CLASSIFY_OUT0 is a specific version of FWPS_CLASSIFY_OUT. |
| [FWPS_DISCARD_METADATA0_ structure](..\fwpstypes\ns-fwpstypes-fwps_discard_metadata0_.md) | The FWPS_DISCARD_METADATA0 structure describes the data that was discarded by the filter engine, a network layer, or a transport layer.Note  FWPS_DISCARD_METADATA0 is a specific version of FWPS_DISCARD_METADATA. |
| [FWPS_FILTER0_ structure](..\fwpstypes\ns-fwpstypes-fwps_filter0_.md) | The FWPS_FILTER0 structure defines a run-time filter in the filter engine.Note  FWPS_FILTER0 is the specific version of FWPS_FILTER used in Windows Vista and later. |
| [FWPS_FILTER1_ structure](..\fwpstypes\ns-fwpstypes-fwps_filter1_.md) | The FWPS_FILTER1 structure defines a run-time filter in the filter engine.Note  FWPS_FILTER1 is the specific version of FWPS_FILTER used in Windows 7 and later. |
| [FWPS_FILTER2_ structure](..\fwpstypes\ns-fwpstypes-fwps_filter2_.md) | The FWPS_FILTER2 structure defines a run-time filter in the filter engine.Note  FWPS_FILTER2 is the specific version of FWPS_FILTER used in Windows 8 and later. |
| [FWPS_FILTER_CONDITION0_ structure](..\fwpstypes\ns-fwpstypes-fwps_filter_condition0_.md) | The FWPS_FILTER_CONDITION0 structure defines a run-time filtering condition for a filter.Note  FWPS_FILTER_CONDITION0 is a specific version of FWPS_FILTER_CONDITION. |
| [FWPS_INBOUND_FRAGMENT_METADATA0_ structure](..\fwpstypes\ns-fwpstypes-fwps_inbound_fragment_metadata0_.md) | The FWPS_INBOUND_FRAGMENT_METADATA0 structure describes the fragment data for a received packet fragment.Note  FWPS_INBOUND_FRAGMENT_METADATA0 is a specific version of FWPS_INBOUND_FRAGMENT_METADATA. |
| [FWPS_INCOMING_VALUE0_ structure](..\fwpstypes\ns-fwpstypes-fwps_incoming_value0_.md) | The FWPS_INCOMING_VALUE0 structure defines an individual data value.Note  FWPS_INCOMING_VALUE0 is a specific version of FWPS_INCOMING_VALUE. |
| [FWPS_INCOMING_VALUES0_ structure](..\fwpstypes\ns-fwpstypes-fwps_incoming_values0_.md) | The FWPS_INCOMING_VALUES0 structure defines data values that are passed by the filter engine to a callout's classifyFn callout function.Note  FWPS_INCOMING_VALUES0 is a specific version of FWPS_INCOMING_VALUES. |
| [NDK_VERSION structure](..\ndkinfo\ns-ndkinfo-ndk_version.md) | The NDK_VERSION structure specifies major and minor versions in the NDK interface. |
| [_L2_NOTIFICATION_DATA structure](..\l2cmn\ns-l2cmn-_l2_notification_data.md) | Important  The Native 802.11 Wireless LAN interface is deprecated in Windows 10 and later. |
| [_NDK_ADAPTER_INFO structure](..\ndkinfo\ns-ndkinfo-_ndk_adapter_info.md) | The NDK_ADAPTER_INFO structure specifies information about limits and capabilities of an NDK adapter. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [FWPS_DISCARD_MODULE0_ enumeration](..\fwpstypes\ne-fwpstypes-fwps_discard_module0_.md) | The FWPS_DISCARD_MODULE0 enumeration type specifies the type of module that discarded the data.Note  FWPS_DISCARD_MODULE0 is a specific version of FWPS_DISCARD_MODULE. |
