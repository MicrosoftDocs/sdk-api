---
UID: NF:netioapi.SetInterfaceDnsSettings
title: SetInterfaceDnsSettings
description: Sets the per-interface DNS settings specified in the *Settings* parameter.
tech.root: IpHlp
ms.date: 07/15/2021
req.construct-type: function
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 19041
req.target-min-winversvr: Windows 10 Build 19041
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - SetInterfaceDnsSettings
 - netioapi/SetInterfaceDnsSettings
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - SetInterfaceDnsSettings
---

## -description

Sets the per-interface DNS settings specified in the *Settings* parameter.

## -parameters

### -param Interface

Type: \_In\_ **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The **GUID** of the COM interface that the settings refer to.

### -param Settings

Type: \_In\_ const **[DNS_INTERFACE_SETTINGS](ns-netioapi-dns_interface_settings.md)\***

A pointer to a **DNS_INTERFACE_SETTINGS**-type structure that contains the DNS interface settings.

If this parameter points to a [**DNS_INTERFACE_SETTINGS**](ns-netioapi-dns_interface_settings.md) structure, then the **DNS_INTERFACE_SETTINGS::Version** member must be set to **DNS_INTERFACE_SETTINGS_VERSION1**.

If this parameter points to a [**DNS_INTERFACE_SETTINGS_EX**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings_ex) structure, then the version must be set to **DNS_INTERFACE_SETTINGS_VERSION2**.

If this parameter points to a [**DNS_INTERFACE_SETTINGS3** ](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings3) structure, then the version must to be set to **DNS_INTERFACE_SETTINGS_VERSION3**.

You must set appropriately all the desired options in the **DNS_INTERFACE_SETTINGS::Flags** field, and populate only the fields for which an option was set. You must zero out all other fields that don't have a corresponding option.

## -returns

Returns **NO_ERROR** if successful. A non-zero return value indicates failure.

## -remarks

## -see-also

* [GetInterfaceDnsSettings](nf-netioapi-getinterfacednssettings.md)