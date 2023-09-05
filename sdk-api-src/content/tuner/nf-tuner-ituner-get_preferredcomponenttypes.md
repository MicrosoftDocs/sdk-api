---
UID: NF:tuner.ITuner.get_PreferredComponentTypes
title: ITuner::get_PreferredComponentTypes (tuner.h)
description: The get_PreferredComponentTypes method gets the collection of ComponentType objects used for default component selection.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","get_PreferredComponentTypes method","ITuner.get_PreferredComponentTypes","ITuner::get_PreferredComponentTypes","ITunerget_PreferredComponentTypes","get_PreferredComponentTypes","get_PreferredComponentTypes method [Microsoft TV Technologies]","get_PreferredComponentTypes method [Microsoft TV Technologies]","ITuner interface","mstv.ituner_get_preferredcomponenttypes","tuner/ITuner::get_PreferredComponentTypes"]
old-location: mstv\ituner_get_preferredcomponenttypes.htm
tech.root: mstv
ms.assetid: 1ed2d1b5-8ba3-4230-8cc3-f8207635a78a
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],get_PreferredComponentTypes method, ITuner.get_PreferredComponentTypes, ITuner::get_PreferredComponentTypes, ITunerget_PreferredComponentTypes, get_PreferredComponentTypes, get_PreferredComponentTypes method [Microsoft TV Technologies], get_PreferredComponentTypes method [Microsoft TV Technologies],ITuner interface, mstv.ituner_get_preferredcomponenttypes, tuner/ITuner::get_PreferredComponentTypes
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
 - ITuner::get_PreferredComponentTypes
 - tuner/ITuner::get_PreferredComponentTypes
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
 - ITuner.get_PreferredComponentTypes
---

# ITuner::get_PreferredComponentTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_PreferredComponentTypes</b> method gets the collection of ComponentType objects used for default component selection.

## -parameters

### -param ComponentTypes [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes</a> interface pointer that receives the collection of ComponentType objects.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When a program ends, there may be a new set of stream components available, so at that time the tuner will automatically examine the list of preferred component types and select a component based on that list. If no list is available, the tuner will make a selection based on other factors. Applications call this method simply to examine the current list.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>