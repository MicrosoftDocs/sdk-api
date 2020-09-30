---
UID: NF:wmp.IWMPEvents3.CdromBurnStateChange
title: IWMPEvents3::CdromBurnStateChange (wmp.h)
description: The CdromBurnStateChange event occurs when a CD burning operation changes state.
helpviewer_keywords: ["CdromBurnStateChange","CdromBurnStateChange method [Windows Media Player]","CdromBurnStateChange method [Windows Media Player]","IWMPEvents3 interface","IWMPEvents3 interface [Windows Media Player]","CdromBurnStateChange method","IWMPEvents3.CdromBurnStateChange","IWMPEvents3::CdromBurnStateChange","IWMPEvents3CdromBurnStateChange","wmp.iwmpevents3_iwmpevents3__cdromburnstatechange","wmp/IWMPEvents3::CdromBurnStateChange"]
old-location: wmp\iwmpevents3_iwmpevents3__cdromburnstatechange.htm
tech.root: WMP
ms.assetid: 8328f1bf-c928-4504-859f-f1b62e77e9e0
ms.date: 12/05/2018
ms.keywords: CdromBurnStateChange, CdromBurnStateChange method [Windows Media Player], CdromBurnStateChange method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromBurnStateChange method, IWMPEvents3.CdromBurnStateChange, IWMPEvents3::CdromBurnStateChange, IWMPEvents3CdromBurnStateChange, wmp.iwmpevents3_iwmpevents3__cdromburnstatechange, wmp/IWMPEvents3::CdromBurnStateChange
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents3::CdromBurnStateChange
 - wmp/IWMPEvents3::CdromBurnStateChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.CdromBurnStateChange
---

# IWMPEvents3::CdromBurnStateChange


## -description

The <b>CdromBurnStateChange</b> event occurs when a CD burning operation changes state.

## -parameters

### -param pCdromBurn [in]

Pointer to the <b>IWMPCdromBurn</b> interface that represents the burning operation that raised the event.

### -param wmpbs [in]

<b>WMPBurnState</b> enumeration value that indicates the new state.

## -remarks

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpburnstate">WMPBurnState</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>