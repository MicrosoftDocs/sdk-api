---
UID: NF:tuner.ITunerCap.get_SupportedNetworkTypes
title: ITunerCap::get_SupportedNetworkTypes (tuner.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ITunerCap interface [Microsoft TV Technologies]","get_SupportedNetworkTypes method","ITunerCap.get_SupportedNetworkTypes","ITunerCap::get_SupportedNetworkTypes","ITunerCapget_SupportedNetworkTypes","get_SupportedNetworkTypes","get_SupportedNetworkTypes method [Microsoft TV Technologies]","get_SupportedNetworkTypes method [Microsoft TV Technologies]","ITunerCap interface","mstv.itunercap_get_supportednetworktypes","tuner/ITunerCap::get_SupportedNetworkTypes"]
old-location: mstv\itunercap_get_supportednetworktypes.htm
tech.root: mstv
ms.assetid: 9763a977-c19a-4e6e-bcd6-93dabd357fbe
ms.date: 12/05/2018
ms.keywords: ITunerCap interface [Microsoft TV Technologies],get_SupportedNetworkTypes method, ITunerCap.get_SupportedNetworkTypes, ITunerCap::get_SupportedNetworkTypes, ITunerCapget_SupportedNetworkTypes, get_SupportedNetworkTypes, get_SupportedNetworkTypes method [Microsoft TV Technologies], get_SupportedNetworkTypes method [Microsoft TV Technologies],ITunerCap interface, mstv.itunercap_get_supportednetworktypes, tuner/ITunerCap::get_SupportedNetworkTypes
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITunerCap::get_SupportedNetworkTypes
 - tuner/ITunerCap::get_SupportedNetworkTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITunerCap.get_SupportedNetworkTypes
---

# ITunerCap::get_SupportedNetworkTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>get_SupportedNetworkTypes</b> method retrieves a list of the network types that are supported by the TV tuner.

## -parameters

### -param ulcNetworkTypesMax [in]

The maximum number of network-type GUIDs that the <i>pguidNetworkTypes</i> buffer can hold.

### -param pulcNetworkTypes [out]

Receives a count of the number of network-type GUIDs actually written to the <i>pguidNetworkTypes</i> buffer.

### -param pguidNetworkTypes [in, out]

Receives an array of network-type GUIDs. For the list of valid network-type GUIDs, see <a href="/previous-versions/windows/desktop/mstv/default-tuning-spaces">Default Tuning Spaces</a>.

## -returns

When the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-itunercap">ITunerCap Interface</a>