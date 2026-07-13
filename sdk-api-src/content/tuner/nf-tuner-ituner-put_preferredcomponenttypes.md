---
UID: NF:tuner.ITuner.put_PreferredComponentTypes
title: ITuner::put_PreferredComponentTypes (tuner.h)
description: The put_PreferredComponentTypes method sets the collection of ComponentType objects used for default component selection.
helpviewer_keywords: ["ITuner interface [Microsoft TV Technologies]","put_PreferredComponentTypes method","ITuner.put_PreferredComponentTypes","ITuner::put_PreferredComponentTypes","ITunerput_PreferredComponentTypes","mstv.ituner_put_preferredcomponenttypes","put_PreferredComponentTypes","put_PreferredComponentTypes method [Microsoft TV Technologies]","put_PreferredComponentTypes method [Microsoft TV Technologies]","ITuner interface","tuner/ITuner::put_PreferredComponentTypes"]
old-location: mstv\ituner_put_preferredcomponenttypes.htm
tech.root: mstv
ms.assetid: cca12a71-c842-4340-9233-f4143f6e0eea
ms.date: 12/05/2018
ms.keywords: ITuner interface [Microsoft TV Technologies],put_PreferredComponentTypes method, ITuner.put_PreferredComponentTypes, ITuner::put_PreferredComponentTypes, ITunerput_PreferredComponentTypes, mstv.ituner_put_preferredcomponenttypes, put_PreferredComponentTypes, put_PreferredComponentTypes method [Microsoft TV Technologies], put_PreferredComponentTypes method [Microsoft TV Technologies],ITuner interface, tuner/ITuner::put_PreferredComponentTypes
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
 - ITuner::put_PreferredComponentTypes
 - tuner/ITuner::put_PreferredComponentTypes
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
 - ITuner.put_PreferredComponentTypes
---

# ITuner::put_PreferredComponentTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_PreferredComponentTypes</b> method sets the collection of <b>ComponentType</b> objects used for default component selection.

## -parameters

### -param ComponentTypes [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes</a> interface that contains the collection of ComponentType objects.

## -returns

When the method is successful, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications create a list of preferred component types by instantiating an empty <b>ComponentTypes</b> collection, filling it, then submitting it to the Tuner using <b>put_PreferredComponentTypes</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituner">ITuner Interface</a>