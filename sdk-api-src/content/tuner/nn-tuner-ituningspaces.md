---
UID: NN:tuner.ITuningSpaces
title: ITuningSpaces (tuner.h)
description: The ITuningSpaces interface represents a collection of tuning spaces.
helpviewer_keywords: ["ITuningSpaces","ITuningSpaces interface [Microsoft TV Technologies]","ITuningSpaces interface [Microsoft TV Technologies]","described","ITuningSpacesInterface","mstv.ituningspaces","tuner/ITuningSpaces"]
old-location: mstv\ituningspaces.htm
tech.root: mstv
ms.assetid: db252e22-8efe-4bfc-8fd3-2be7022bbbbd
ms.date: 12/05/2018
ms.keywords: ITuningSpaces, ITuningSpaces interface [Microsoft TV Technologies], ITuningSpaces interface [Microsoft TV Technologies],described, ITuningSpacesInterface, mstv.ituningspaces, tuner/ITuningSpaces
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
 - ITuningSpaces
 - tuner/ITuningSpaces
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
 - ITuningSpaces
---

# ITuningSpaces interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ITuningSpaces</b> interface represents a collection of tuning spaces.

## -inheritance

The <b>ITuningSpaces</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuningSpaces</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

This interface is used to enumerate subsets of tuning spaces within the <a href="/previous-versions/windows/desktop/mstv/systemtuningspaces-object">SystemTuningSpaces</a> object. To enumerate all of the tuning spaces available on the system, use the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a> interface on the SystemTuningSpaces object.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpaces)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
