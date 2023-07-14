---
UID: NF:tuner.IComponents.get_Count
title: IComponents::get_Count (tuner.h)
description: The get_Count method gets the number of Component objects in the collection.
helpviewer_keywords: ["IComponents interface [Microsoft TV Technologies]","get_Count method","IComponents.get_Count","IComponents::get_Count","IComponentsget_Count","get_Count","get_Count method [Microsoft TV Technologies]","get_Count method [Microsoft TV Technologies]","IComponents interface","mstv.icomponents_get_count","tuner/IComponents::get_Count"]
old-location: mstv\icomponents_get_count.htm
tech.root: mstv
ms.assetid: ba198e27-c699-4c93-aa2d-b8be8c40380c
ms.date: 12/05/2018
ms.keywords: IComponents interface [Microsoft TV Technologies],get_Count method, IComponents.get_Count, IComponents::get_Count, IComponentsget_Count, get_Count, get_Count method [Microsoft TV Technologies], get_Count method [Microsoft TV Technologies],IComponents interface, mstv.icomponents_get_count, tuner/IComponents::get_Count
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
 - IComponents::get_Count
 - tuner/IComponents::get_Count
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
 - IComponents.get_Count
---

# IComponents::get_Count


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Count</b> method gets the number of <b>Component</b> objects in the collection.

## -parameters

### -param Count [out]

Pointer to a variable of type <b>long</b> that receives the number of components.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>