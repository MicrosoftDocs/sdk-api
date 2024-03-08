---
UID: NN:tuner.ITuningSpace
title: ITuningSpace (tuner.h)
description: The ITuningSpace interface provides the common functionality for all network-specific tuning spaces.
helpviewer_keywords: ["ITuningSpace","ITuningSpace interface [Microsoft TV Technologies]","ITuningSpace interface [Microsoft TV Technologies]","described","ITuningSpaceInterface","mstv.ituningspace","tuner/ITuningSpace"]
old-location: mstv\ituningspace.htm
tech.root: mstv
ms.assetid: 51850105-b3b1-4758-acde-05ca2f3439f2
ms.date: 12/05/2018
ms.keywords: ITuningSpace, ITuningSpace interface [Microsoft TV Technologies], ITuningSpace interface [Microsoft TV Technologies],described, ITuningSpaceInterface, mstv.ituningspace, tuner/ITuningSpace
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
 - ITuningSpace
 - tuner/ITuningSpace
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
 - ITuningSpace
---

# ITuningSpace interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ITuningSpace</b> interface provides the common functionality for all network-specific tuning spaces. Applications can obtain tuning spaces from the <a href="/previous-versions/windows/desktop/mstv/systemtuningspaces-object">SystemTuningSpaces</a> collection. A tuning space generally exposes an interface that inherits <b>ITuningSpace</b>, such as <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>.

## -inheritance

The <b>ITuningSpace</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITuningSpace</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpace)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
