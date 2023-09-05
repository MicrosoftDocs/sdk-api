---
UID: NF:tuner.IComponentType.get_Category
title: IComponentType::get_Category (tuner.h)
description: The get_Category method retrieves the component category.
helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","get_Category method","IComponentType.get_Category","IComponentType::get_Category","IComponentTypeget_Category","get_Category","get_Category method [Microsoft TV Technologies]","get_Category method [Microsoft TV Technologies]","IComponentType interface","mstv.icomponenttype_get_category","tuner/IComponentType::get_Category"]
old-location: mstv\icomponenttype_get_category.htm
tech.root: mstv
ms.assetid: e0a61359-a15a-47f6-8388-90368867e945
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],get_Category method, IComponentType.get_Category, IComponentType::get_Category, IComponentTypeget_Category, get_Category, get_Category method [Microsoft TV Technologies], get_Category method [Microsoft TV Technologies],IComponentType interface, mstv.icomponenttype_get_category, tuner/IComponentType::get_Category
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
 - IComponentType::get_Category
 - tuner/IComponentType::get_Category
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
 - IComponentType.get_Category
---

# IComponentType::get_Category


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Category</b> method retrieves the component category.

## -parameters

### -param Category [out]

Pointer to a <a href="/previous-versions/windows/desktop/mstv/componentcategory">ComponentCategory</a> data type that will receive the category.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>