---
UID: NF:tuner.IDVBTLocator.put_Mode
title: IDVBTLocator::put_Mode (tuner.h)
description: The put_Mode method sets the transmission mode.
helpviewer_keywords: ["IDVBTLocator interface [Microsoft TV Technologies]","put_Mode method","IDVBTLocator.put_Mode","IDVBTLocator::put_Mode","IDVBTLocatorput_Mode","mstv.idvbtlocator_put_mode","put_Mode","put_Mode method [Microsoft TV Technologies]","put_Mode method [Microsoft TV Technologies]","IDVBTLocator interface","tuner/IDVBTLocator::put_Mode"]
old-location: mstv\idvbtlocator_put_mode.htm
tech.root: mstv
ms.assetid: 762f4604-46c9-4c19-9621-5ede52d8f524
ms.date: 12/05/2018
ms.keywords: IDVBTLocator interface [Microsoft TV Technologies],put_Mode method, IDVBTLocator.put_Mode, IDVBTLocator::put_Mode, IDVBTLocatorput_Mode, mstv.idvbtlocator_put_mode, put_Mode, put_Mode method [Microsoft TV Technologies], put_Mode method [Microsoft TV Technologies],IDVBTLocator interface, tuner/IDVBTLocator::put_Mode
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDVBTLocator::put_Mode
 - tuner/IDVBTLocator::put_Mode
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
 - IDVBTLocator.put_Mode
---

# IDVBTLocator::put_Mode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Mode</b> method sets the transmission mode.

## -parameters

### -param mode [in]

Specifies the transmission mode as a member of the <a href="/previous-versions/windows/desktop/mstv/transmissionmode">TransmissionMode</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtlocator">IDVBTLocator Interface</a>