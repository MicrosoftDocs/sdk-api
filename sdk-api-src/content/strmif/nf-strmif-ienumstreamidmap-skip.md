---
UID: NF:strmif.IEnumStreamIdMap.Skip
title: IEnumStreamIdMap::Skip (strmif.h)
description: The Skip method skip the element at the specified index.
helpviewer_keywords: ["IEnumStreamIdMap interface [DirectShow]","Skip method","IEnumStreamIdMap.Skip","IEnumStreamIdMap::Skip","IEnumStreamIdMapSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumStreamIdMap interface","dshow.ienumstreamidmap_skip","strmif/IEnumStreamIdMap::Skip"]
old-location: dshow\ienumstreamidmap_skip.htm
tech.root: dshow
ms.assetid: 54502cd5-50b2-4bd2-a13f-180bddac178a
ms.date: 12/05/2018
ms.keywords: IEnumStreamIdMap interface [DirectShow],Skip method, IEnumStreamIdMap.Skip, IEnumStreamIdMap::Skip, IEnumStreamIdMapSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumStreamIdMap interface, dshow.ienumstreamidmap_skip, strmif/IEnumStreamIdMap::Skip
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumStreamIdMap::Skip
 - strmif/IEnumStreamIdMap::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IEnumStreamIdMap.Skip
---

# IEnumStreamIdMap::Skip


## -description

The <code>Skip</code> method skip the element at the specified index.

## -parameters

### -param cRecords [in]

Index of the element to skip.

## -returns

Returns S_OK if successful. If the method fails, an <b>HRESULT</b> error code is returned.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ienumstreamidmap">IEnumStreamIdMap Interface</a>