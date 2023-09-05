---
UID: NF:tuner.IComponentType.Clone
title: IComponentType::Clone (tuner.h)
description: The Clone method creates a new copy of this component type.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","IComponentType interface","IComponentType interface [Microsoft TV Technologies]","Clone method","IComponentType.Clone","IComponentType::Clone","IComponentTypeClone","mstv.icomponenttype_clone","tuner/IComponentType::Clone"]
old-location: mstv\icomponenttype_clone.htm
tech.root: mstv
ms.assetid: 34cab0cb-8b38-4d03-be2a-ef14bd9505f2
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IComponentType interface, IComponentType interface [Microsoft TV Technologies],Clone method, IComponentType.Clone, IComponentType::Clone, IComponentTypeClone, mstv.icomponenttype_clone, tuner/IComponentType::Clone
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
 - IComponentType::Clone
 - tuner/IComponentType::Clone
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
 - IComponentType.Clone
---

# IComponentType::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a new copy of this component type.

## -parameters

### -param NewCT [out]

Address of the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface pointer that will be set to the returned interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>