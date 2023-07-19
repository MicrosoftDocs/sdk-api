---
UID: NF:tuner.IComponents.Clone
title: IComponents::Clone (tuner.h)
description: The Clone method creates a new copy of the collection.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","IComponents interface","IComponents interface [Microsoft TV Technologies]","Clone method","IComponents.Clone","IComponents::Clone","IComponentsClone","mstv.icomponents_clone","tuner/IComponents::Clone"]
old-location: mstv\icomponents_clone.htm
tech.root: mstv
ms.assetid: 5a98e265-8bef-4978-a257-1519006e9124
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponents interface, IComponents interface [Microsoft TV Technologies],Clone method, IComponents.Clone, IComponents::Clone, IComponentsClone, mstv.icomponents_clone, tuner/IComponents::Clone
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
 - IComponents::Clone
 - tuner/IComponents::Clone
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
 - IComponents.Clone
---

# IComponents::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a new copy of the collection.

## -parameters

### -param NewList [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> interface pointer that will be set to the new <b>Components</b> object.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>