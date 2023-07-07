---
UID: NF:tuner.IComponents.Add
title: IComponents::Add (tuner.h)
description: The Add method adds a Component object to the collection.
helpviewer_keywords: ["Add","Add method [Microsoft TV Technologies]","Add method [Microsoft TV Technologies]","IComponents interface","IComponents interface [Microsoft TV Technologies]","Add method","IComponents.Add","IComponents::Add","IComponentsAdd","mstv.icomponents_add","tuner/IComponents::Add"]
old-location: mstv\icomponents_add.htm
tech.root: mstv
ms.assetid: ec5d9d6c-4957-46f2-9798-6e30c934459e
ms.date: 12/05/2018
ms.keywords: Add, Add method [Microsoft TV Technologies], Add method [Microsoft TV Technologies],IComponents interface, IComponents interface [Microsoft TV Technologies],Add method, IComponents.Add, IComponents::Add, IComponentsAdd, mstv.icomponents_add, tuner/IComponents::Add
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
 - IComponents::Add
 - tuner/IComponents::Add
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
 - IComponents.Add
---

# IComponents::Add


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Add</b> method adds a <b>Component</b> object to the collection.

## -parameters

### -param Component [in]

Pointer to the <b>Component</b> object to be added.

### -param NewIndex [out]

Pointer to a <b>VARIANT</b> that will receive the index of the <b>Component</b> object after it has been added.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents Interface</a>