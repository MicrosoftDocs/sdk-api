---
UID: NF:tuner.IComponentType.put_Category
title: IComponentType::put_Category (tuner.h)
description: The put_Category method sets the component category.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put_Category method","IComponentType.put_Category","IComponentType::put_Category","IComponentTypeput_Category","mstv.icomponenttype_put_category","put_Category","put_Category method [Microsoft TV Technologies]","put_Category method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put_Category"]
old-location: mstv\icomponenttype_put_category.htm
tech.root: mstv
ms.assetid: 3ae90ec5-ebae-4a67-b786-33a1d94309b8
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_Category method, IComponentType.put_Category, IComponentType::put_Category, IComponentTypeput_Category, mstv.icomponenttype_put_category, put_Category, put_Category method [Microsoft TV Technologies], put_Category method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_Category
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
 - IComponentType::put_Category
 - tuner/IComponentType::put_Category
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
 - IComponentType.put_Category
---

# IComponentType::put_Category


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Category</b> method sets the component category.

## -parameters

### -param Category [in]

A <a href="/previous-versions/windows/desktop/mstv/componentcategory">ComponentCategory</a> value that specifies the new category for this component type.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>