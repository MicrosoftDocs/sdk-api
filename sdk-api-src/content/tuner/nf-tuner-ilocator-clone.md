---
UID: NF:tuner.ILocator.Clone
title: ILocator::Clone (tuner.h)
description: The Clone method creates a copy of the Locator.
helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","ILocator interface","ILocator interface [Microsoft TV Technologies]","Clone method","ILocator.Clone","ILocator::Clone","ILocatorClone","mstv.ilocator_clone","tuner/ILocator::Clone"]
old-location: mstv\ilocator_clone.htm
tech.root: mstv
ms.assetid: 9a1fd730-80b9-439b-aab2-069710aa3dfa
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ILocator interface, ILocator interface [Microsoft TV Technologies],Clone method, ILocator.Clone, ILocator::Clone, ILocatorClone, mstv.ilocator_clone, tuner/ILocator::Clone
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
 - ILocator::Clone
 - tuner/ILocator::Clone
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
 - ILocator.Clone
---

# ILocator::Clone


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Clone</b> method creates a copy of the Locator.

## -parameters

### -param NewLocator [out]

Receives a pointer to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a> interface. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator Interface</a>