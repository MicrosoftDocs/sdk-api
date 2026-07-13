---
UID: NF:comcat.IEnumCATEGORYINFO.Skip
title: IEnumCATEGORYINFO::Skip (comcat.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumCATEGORYINFO.Skip)
helpviewer_keywords: ["IEnumCATEGORYINFO interface [COM]","Skip method","IEnumCATEGORYINFO.Skip","IEnumCATEGORYINFO::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumCATEGORYINFO interface","_com_ienumcategoryinfo_skip","com.ienumcategoryinfo_skip","comcat/IEnumCATEGORYINFO::Skip"]
old-location: com\ienumcategoryinfo_skip.htm
tech.root: com
ms.assetid: 405a506b-8bce-47ea-a5a7-6cd7146dcef3
ms.date: 12/05/2018
ms.keywords: IEnumCATEGORYINFO interface [COM],Skip method, IEnumCATEGORYINFO.Skip, IEnumCATEGORYINFO::Skip, Skip, Skip method [COM], Skip method [COM],IEnumCATEGORYINFO interface, _com_ienumcategoryinfo_skip, com.ienumcategoryinfo_skip, comcat/IEnumCATEGORYINFO::Skip
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Comcat.idl
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
 - IEnumCATEGORYINFO::Skip
 - comcat/IEnumCATEGORYINFO::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComCat.h
api_name:
 - IEnumCATEGORYINFO.Skip
---

# IEnumCATEGORYINFO::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-ienumcategoryinfo">IEnumCATEGORYINFO</a>
