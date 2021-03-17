---
UID: NF:wmp.IWMPEvents3.CdromBurnError
title: IWMPEvents3::CdromBurnError (wmp.h)
description: The CdromBurnError event occurs when a generic error happens during a CD burning operation.
helpviewer_keywords: ["CdromBurnError","CdromBurnError method [Windows Media Player]","CdromBurnError method [Windows Media Player]","IWMPEvents3 interface","IWMPEvents3 interface [Windows Media Player]","CdromBurnError method","IWMPEvents3.CdromBurnError","IWMPEvents3::CdromBurnError","IWMPEvents3CdromBurnError","wmp.iwmpevents3_iwmpevents3__cdromburnerror","wmp/IWMPEvents3::CdromBurnError"]
old-location: wmp\iwmpevents3_iwmpevents3__cdromburnerror.htm
tech.root: WMP
ms.assetid: ea1ded30-4fca-4208-9fc2-f93c169f33b6
ms.date: 12/05/2018
ms.keywords: CdromBurnError, CdromBurnError method [Windows Media Player], CdromBurnError method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromBurnError method, IWMPEvents3.CdromBurnError, IWMPEvents3::CdromBurnError, IWMPEvents3CdromBurnError, wmp.iwmpevents3_iwmpevents3__cdromburnerror, wmp/IWMPEvents3::CdromBurnError
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
 - IWMPEvents3::CdromBurnError
 - wmp/IWMPEvents3::CdromBurnError
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
 - IWMPEvents3.CdromBurnError
---

# IWMPEvents3::CdromBurnError


## -description

The <b>CdromBurnError</b> event occurs when a generic error happens during a CD burning operation.

## -parameters

### -param pCdromBurn [in]

Pointer to the <b>IWMPCdromBurn</b> interface that represents the burning operation that raised the error.

### -param hrError [in]

<b>HRESULT</b> for the error that raised the event.

## -remarks

To capture media specific errors, handle the <b>CdromBurnMediaError</b> event.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror">IWMPEvents3::CdromBurnMediaError</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>