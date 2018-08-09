---
UID: NS:wsdbase._WSD_CONFIG_ADDRESSES
title: "_WSD_CONFIG_ADDRESSES"
author: windows-sdk-content
description: Information about specific addresses that a host should listen on.
old-location: ncd\wsd_config_addresses.htm
old-project: wsdapi
ms.assetid: aaec97f4-c0b9-49d3-ab4c-758feda15d6a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWSD_CONFIG_ADDRESSES, WSD_CONFIG_ADDRESSES, WSD_CONFIG_ADDRESSES structure, _WSD_CONFIG_ADDRESSES, ncd.wsd_config_addresses, wsdbase/WSD_CONFIG_ADDRESSES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wsdbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_ADDRESSES, *PWSD_CONFIG_ADDRESSES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wsdbase.h
api_name:
 - WSD_CONFIG_ADDRESSES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WSD_CONFIG_ADDRESSES structure


## -description


Information about specific addresses that a host should listen on.


## -struct-fields




### -field addresses

An array of pointers to <a href="https://msdn.microsoft.com/b19938b2-2fba-42fe-8c4e-5696c40acd58">IWSDAddress</a> interfaces.

If <i>pszLocalId</i> contains a logical address, the resulting behavior is a mapping between the logical address and a specific set of physical addresses (instead of a mapping between the logical address and a default physical address).


### -field dwAddressCount

The number of items in the <b>addresses</b> array.

