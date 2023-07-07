---
UID: NN:tuner.IComponents
title: IComponents (tuner.h)
description: The IComponents interface represents a collection of components.
helpviewer_keywords: ["IComponents","IComponents interface [Microsoft TV Technologies]","IComponents interface [Microsoft TV Technologies]","described","IComponentsInterface","mstv.icomponents","tuner/IComponents"]
old-location: mstv\icomponents.htm
tech.root: mstv
ms.assetid: 670b47ba-bcbd-4281-95e3-a5d784f0610b
ms.date: 12/05/2018
ms.keywords: IComponents, IComponents interface [Microsoft TV Technologies], IComponents interface [Microsoft TV Technologies],described, IComponentsInterface, mstv.icomponents, tuner/IComponents
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
 - IComponents
 - tuner/IComponents
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
 - IComponents
---

# IComponents interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IComponents</b> interface represents a collection of components. In digital television, the term <i>component</i> refers to a substream within the program stream. For example, a program stream may have three audio streams in different languages; in this case each audio stream is a component of the program stream. The <b>IComponents</b> interface is implemented on the Components object, which is a collection of components. The Components object enables applications to enumerate components within a program stream and perform operations related to individual components in the collection. The Components object also supports <b>IPersistPropertyBag</b>.

## -inheritance

The <b>IComponents</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IComponents</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponents)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
