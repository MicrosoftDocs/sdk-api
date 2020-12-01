---
UID: NS:wsdbase._WSD_CONFIG_ADDRESSES
title: WSD_CONFIG_ADDRESSES (wsdbase.h)
description: Information about specific addresses that a host should listen on.
helpviewer_keywords: ["*PWSD_CONFIG_ADDRESSES","WSD_CONFIG_ADDRESSES","WSD_CONFIG_ADDRESSES structure","_WSD_CONFIG_ADDRESSES","ncd.wsd_config_addresses","wsdbase/WSD_CONFIG_ADDRESSES"]
old-location: ncd\wsd_config_addresses.htm
tech.root: ncd
ms.assetid: aaec97f4-c0b9-49d3-ab4c-758feda15d6a
ms.date: 12/05/2018
ms.keywords: '*PWSD_CONFIG_ADDRESSES, WSD_CONFIG_ADDRESSES, WSD_CONFIG_ADDRESSES structure, _WSD_CONFIG_ADDRESSES, ncd.wsd_config_addresses, wsdbase/WSD_CONFIG_ADDRESSES'
req.header: wsdbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WSD_CONFIG_ADDRESSES, *PWSD_CONFIG_ADDRESSES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSD_CONFIG_ADDRESSES
 - wsdbase/_WSD_CONFIG_ADDRESSES
 - PWSD_CONFIG_ADDRESSES
 - wsdbase/PWSD_CONFIG_ADDRESSES
 - WSD_CONFIG_ADDRESSES
 - wsdbase/WSD_CONFIG_ADDRESSES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wsdbase.h
api_name:
 - WSD_CONFIG_ADDRESSES
---

# WSD_CONFIG_ADDRESSES structure


## -description

Information about specific addresses that a host should listen on.

## -struct-fields

### -field addresses

An array of pointers to <a href="/windows/desktop/api/wsdbase/nn-wsdbase-iwsdaddress">IWSDAddress</a> interfaces.

If <i>pszLocalId</i> contains a logical address, the resulting behavior is a mapping between the logical address and a specific set of physical addresses (instead of a mapping between the logical address and a default physical address).

### -field dwAddressCount

The number of items in the <b>addresses</b> array.