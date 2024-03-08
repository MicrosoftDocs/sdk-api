---
UID: NF:tuner.ILocator.put_Modulation
title: ILocator::put_Modulation (tuner.h)
description: The put_Modulation method sets the modulation type.
helpviewer_keywords: ["ILocator interface [Microsoft TV Technologies]","put_Modulation method","ILocator.put_Modulation","ILocator::put_Modulation","ILocatorput_Modulation","mstv.ilocator_put_modulation","put_Modulation","put_Modulation method [Microsoft TV Technologies]","put_Modulation method [Microsoft TV Technologies]","ILocator interface","tuner/ILocator::put_Modulation"]
old-location: mstv\ilocator_put_modulation.htm
tech.root: mstv
ms.assetid: 84a5b2ce-d26b-4ffc-b757-a799658f2b34
ms.date: 12/05/2018
ms.keywords: ILocator interface [Microsoft TV Technologies],put_Modulation method, ILocator.put_Modulation, ILocator::put_Modulation, ILocatorput_Modulation, mstv.ilocator_put_modulation, put_Modulation, put_Modulation method [Microsoft TV Technologies], put_Modulation method [Microsoft TV Technologies],ILocator interface, tuner/ILocator::put_Modulation
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
 - ILocator::put_Modulation
 - tuner/ILocator::put_Modulation
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
 - ILocator.put_Modulation
---

# ILocator::put_Modulation


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Modulation</b> method sets the modulation type.

## -parameters

### -param Modulation [in]

The modulation type, as a member of the <a href="/previous-versions/windows/desktop/mstv/modulationtype">ModulationType</a> enumeration.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator Interface</a>