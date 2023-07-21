---
UID: NF:tuner.ITuningSpace.get_DefaultPreferredComponentTypes
title: ITuningSpace::get_DefaultPreferredComponentTypes (tuner.h)
description: The get_DefaultPreferredComponentTypes method returns a list of the default preferred component types for this tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","get_DefaultPreferredComponentTypes method","ITuningSpace.get_DefaultPreferredComponentTypes","ITuningSpace::get_DefaultPreferredComponentTypes","ITuningSpaceget_DefaultPreferredComponentTypes","get_DefaultPreferredComponentTypes","get_DefaultPreferredComponentTypes method [Microsoft TV Technologies]","get_DefaultPreferredComponentTypes method [Microsoft TV Technologies]","ITuningSpace interface","mstv.ituningspace_get_defaultpreferredcomponenttypes","tuner/ITuningSpace::get_DefaultPreferredComponentTypes"]
old-location: mstv\ituningspace_get_defaultpreferredcomponenttypes.htm
tech.root: mstv
ms.assetid: a633a94c-e514-46b1-9982-7526ffa89b74
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],get_DefaultPreferredComponentTypes method, ITuningSpace.get_DefaultPreferredComponentTypes, ITuningSpace::get_DefaultPreferredComponentTypes, ITuningSpaceget_DefaultPreferredComponentTypes, get_DefaultPreferredComponentTypes, get_DefaultPreferredComponentTypes method [Microsoft TV Technologies], get_DefaultPreferredComponentTypes method [Microsoft TV Technologies],ITuningSpace interface, mstv.ituningspace_get_defaultpreferredcomponenttypes, tuner/ITuningSpace::get_DefaultPreferredComponentTypes
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
 - ITuningSpace::get_DefaultPreferredComponentTypes
 - tuner/ITuningSpace::get_DefaultPreferredComponentTypes
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
 - ITuningSpace.get_DefaultPreferredComponentTypes
---

# ITuningSpace::get_DefaultPreferredComponentTypes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DefaultPreferredComponentTypes</b> method returns a list of the default preferred component types for this tuning space.

## -parameters

### -param ComponentTypes [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttypes">IComponentTypes</a> interface pointer. Use this interface to enumerate the component types. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

A component is a stream within the program. An example of a preferred component type would be an audio stream in English. When multiple components are available, the Tuner attempts to play the preferred ones first.

If the tuning space does not have any default preferred types, this method succeeds but returns the value <b>NULL</b> in the <i>ppComponentTypes</i> parameter. Check for a <b>NULL</b> value before attempting to dereference the pointer.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>