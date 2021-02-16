---
UID: NF:mediaobj.IEnumDMO.Skip
title: IEnumDMO::Skip (mediaobj.h)
description: The Skip method skips over a specified number of items in the enumeration sequence.
helpviewer_keywords: ["IEnumDMO interface [DirectShow]","Skip method","IEnumDMO.Skip","IEnumDMO::Skip","IEnumDMOSkip","Skip","Skip method [DirectShow]","Skip method [DirectShow]","IEnumDMO interface","dshow.ienumdmo_skip","mediaobj/IEnumDMO::Skip"]
old-location: dshow\ienumdmo_skip.htm
tech.root: dshow
ms.assetid: 32722190-52b5-468a-91d6-a828ad02b203
ms.date: 12/05/2018
ms.keywords: IEnumDMO interface [DirectShow],Skip method, IEnumDMO.Skip, IEnumDMO::Skip, IEnumDMOSkip, Skip, Skip method [DirectShow], Skip method [DirectShow],IEnumDMO interface, dshow.ienumdmo_skip, mediaobj/IEnumDMO::Skip
req.header: mediaobj.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumDMO::Skip
 - mediaobj/IEnumDMO::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IEnumDMO.Skip
---

# IEnumDMO::Skip


## -description

The <code>Skip</code> method skips over a specified number of items in the enumeration sequence.

## -parameters

### -param cItemsToSkip

Number of items to skip.

## -returns

Returns S_OK if the number items skipped equals <i>cItemsToSkip</i>. Otherwise, returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-ienumdmo">IEnumDMO Interface</a>