---
UID: NN:tuner.IEnumTuningSpaces
title: IEnumTuningSpaces (tuner.h)
description: The IEnumTuningSpaces interface is implemented on a standard COM collection of tuning space objects and is obtained through various ITuningSpaceContainer.
helpviewer_keywords: ["IEnumTuningSpaces","IEnumTuningSpaces interface [Microsoft TV Technologies]","IEnumTuningSpaces interface [Microsoft TV Technologies]","described","IEnumTuningSpacesInterface","mstv.ienumtuningspaces","tuner/IEnumTuningSpaces"]
old-location: mstv\ienumtuningspaces.htm
tech.root: mstv
ms.assetid: 9b64a48f-ebab-46af-a89d-b8bc488d85da
ms.date: 12/05/2018
ms.keywords: IEnumTuningSpaces, IEnumTuningSpaces interface [Microsoft TV Technologies], IEnumTuningSpaces interface [Microsoft TV Technologies],described, IEnumTuningSpacesInterface, mstv.ienumtuningspaces, tuner/IEnumTuningSpaces
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
 - IEnumTuningSpaces
 - tuner/IEnumTuningSpaces
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
 - IEnumTuningSpaces
---

# IEnumTuningSpaces interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEnumTuningSpaces</b> interface is implemented on a standard COM collection of tuning space objects and is obtained through various <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a>.

## -inheritance

The <b>IEnumTuningSpaces</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTuningSpaces</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuningSpaces)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
