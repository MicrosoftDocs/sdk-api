---
UID: NF:netioapi.GetInterfaceDnsSettings
title: GetInterfaceDnsSettings
description: Retrieves the DNS settings from the interface specified in the *Interface* parameter.
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
 - GetInterfaceDnsSettings
 - netioapi/GetInterfaceDnsSettings
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetInterfaceDnsSettings
---

## -description

Retrieves the DNS settings from the interface specified in the *Interface* parameter. When you are done with the returned settings object, you must call [FreeInterfaceDnsSettings](nf-netioapi-freeinterfacednssettings.md) to free it.

## -parameters

### -param Interface

Type: \_In\_ **[GUID](/windows/win32/api/guiddef/ns-guiddef-guid)**

The **GUID** of the COM interface that the settings refer to.

### -param Settings

Type: \_Inout\_ const **[DNS_INTERFACE_SETTINGS](ns-netioapi-dns_interface_settings.md)\***

**GetInterfaceDnsSettings** populates all the settings in this structure.

You should set only the *Version* member; the *Flags* field must be empty.

If you set the *Version* member to **DNS_INTERFACE_SETTINGS_VERSION1**, then the *Settings* parameter must point to a valid [**DNS_INTERFACE_SETTINGS**](ns-netioapi-dns_interface_settings.md) structure.

If you set the *Version* member to **DNS_INTERFACE_SETTINGS_VERSION2**, then the *Settings* parameter must point to a valid [**DNS_INTERFACE_SETTINGS_EX**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings_ex) structure.

If you set the *Version* member to **DNS_INTERFACE_SETTINGS_VERSION3**, then the *Settings* parameter must point to a valid [**DNS_INTERFACE_SETTINGS3**](/windows/win32/api/netioapi/ns-netioapi-dns_interface_settings3) structure.

## -returns

Returns **NO_ERROR** if successful. A non-zero return value indicates failure.

## -remarks

## -see-also

* [SetInterfaceDnsSettings](nf-netioapi-setinterfacednssettings.md)
* [FreeInterfaceDnsSettings](nf-netioapi-freeinterfacednssettings.md)
