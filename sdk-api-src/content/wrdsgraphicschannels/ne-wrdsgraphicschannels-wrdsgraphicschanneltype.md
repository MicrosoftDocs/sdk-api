---
UID: NE:wrdsgraphicschannels.__MIDL___MIDL_itf_wrdsgraphicschannels_0000_0002_0001
title: WRdsGraphicsChannelType (wrdsgraphicschannels.h)
description: Used to specify the type of graphics virtual channel to create in the IWRdsGraphicsChannelManager::CreateChannel method.
helpviewer_keywords: ["WRdsGraphicsChannelType","WRdsGraphicsChannelType enumeration [Remote Desktop Services]","WRdsGraphicsChannelType_BestEffortDelivery","WRdsGraphicsChannelType_GuaranteedDelivery","termserv.wrdsgraphicschanneltype","wrdsgraphicschannels/WRdsGraphicsChannelType","wrdsgraphicschannels/WRdsGraphicsChannelType_BestEffortDelivery","wrdsgraphicschannels/WRdsGraphicsChannelType_GuaranteedDelivery"]
old-location: termserv\wrdsgraphicschanneltype.htm
tech.root: TermServ
ms.assetid: 79B63FCD-6BCD-44E6-A5C3-6F5E1336DAA5
ms.date: 12/05/2018
ms.keywords: WRdsGraphicsChannelType, WRdsGraphicsChannelType enumeration [Remote Desktop Services], WRdsGraphicsChannelType_BestEffortDelivery, WRdsGraphicsChannelType_GuaranteedDelivery, termserv.wrdsgraphicschanneltype, wrdsgraphicschannels/WRdsGraphicsChannelType, wrdsgraphicschannels/WRdsGraphicsChannelType_BestEffortDelivery, wrdsgraphicschannels/WRdsGraphicsChannelType_GuaranteedDelivery
req.header: wrdsgraphicschannels.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wrdsgraphicschannels.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WRdsGraphicsChannelType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wrdsgraphicschannels_0000_0002_0001
 - wrdsgraphicschannels/__MIDL___MIDL_itf_wrdsgraphicschannels_0000_0002_0001
 - WRdsGraphicsChannelType
 - wrdsgraphicschannels/WRdsGraphicsChannelType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wrdsgraphicschannels.h
api_name:
 - WRdsGraphicsChannelType
---

# WRdsGraphicsChannelType enumeration


## -description

Used to specify the type of graphics virtual channel to create in the <a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelmanager-createchannel">IWRdsGraphicsChannelManager::CreateChannel</a> method.

## -enum-fields

### -field WRdsGraphicsChannelType_GuaranteedDelivery:0

The channel delivery must be guaranteed.

### -field WRdsGraphicsChannelType_BestEffortDelivery:1

The channel delivery can be lossy.

## -see-also

<a href="/windows/desktop/api/wrdsgraphicschannels/nf-wrdsgraphicschannels-iwrdsgraphicschannelmanager-createchannel">IWRdsGraphicsChannelManager::CreateChannel</a>
