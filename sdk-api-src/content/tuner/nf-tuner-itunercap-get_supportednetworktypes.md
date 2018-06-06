---
UID: NF:tuner.ITunerCap.get_SupportedNetworkTypes
title: ITunerCap::get_SupportedNetworkTypes
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
old-location: mstv\itunercap_get_supportednetworktypes.htm
old-project: mstv
ms.assetid: 9763a977-c19a-4e6e-bcd6-93dabd357fbe
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITunerCap interface [Microsoft TV Technologies],get_SupportedNetworkTypes method, ITunerCap.get_SupportedNetworkTypes, ITunerCap::get_SupportedNetworkTypes, ITunerCapget_SupportedNetworkTypes, get_SupportedNetworkTypes, get_SupportedNetworkTypes method [Microsoft TV Technologies], get_SupportedNetworkTypes method [Microsoft TV Technologies],ITunerCap interface, mstv.itunercap_get_supportednetworktypes, tuner/ITunerCap::get_SupportedNetworkTypes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITunerCap.get_SupportedNetworkTypes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITunerCap::get_SupportedNetworkTypes


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SupportedNetworkTypes</b> method retrieves a list of the network types that are supported by the TV tuner.


## -parameters




### -param ulcNetworkTypesMax [in]

The maximum number of network-type GUIDs that the <i>pguidNetworkTypes</i> buffer can hold.


### -param pulcNetworkTypes [out]

Receives a count of the number of network-type GUIDs actually written to the <i>pguidNetworkTypes</i> buffer.


### -param pguidNetworkTypes [in, out]

Receives an array of network-type GUIDs. For the list of valid network-type GUIDs, see <a href="https://msdn.microsoft.com/627e8aaf-7638-4d17-97b5-0aeaad304b98">Default Tuning Spaces</a>.


## -returns



When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d7027ff4-4fb9-48c1-b527-92e65009b089">ITunerCap Interface</a>
 

 

