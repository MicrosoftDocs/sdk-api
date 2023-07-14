---
UID: NN:tuner.IEnumComponents
title: IEnumComponents (tuner.h)
description: The IEnumComponents interface provides a standard COM enumeration object for the components (substreams) in a given program stream.
helpviewer_keywords: ["IEnumComponents","IEnumComponents interface [Microsoft TV Technologies]","IEnumComponents interface [Microsoft TV Technologies]","described","IEnumComponentsInterface","mstv.ienumcomponents","tuner/IEnumComponents"]
old-location: mstv\ienumcomponents.htm
tech.root: mstv
ms.assetid: 8811021c-8c14-4be6-8802-76b942bb34d8
ms.date: 12/05/2018
ms.keywords: IEnumComponents, IEnumComponents interface [Microsoft TV Technologies], IEnumComponents interface [Microsoft TV Technologies],described, IEnumComponentsInterface, mstv.ienumcomponents, tuner/IEnumComponents
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
 - IEnumComponents
 - tuner/IEnumComponents
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
 - IEnumComponents
---

# IEnumComponents interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IEnumComponents</b> interface provides a standard COM enumeration object for the components (substreams) in a given program stream. C++ applications should use this interface to enumerate components, rather than using the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> collection interface, which is intended for Automation clients.

## -inheritance

The <b>IEnumComponents</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumComponents</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponents)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
