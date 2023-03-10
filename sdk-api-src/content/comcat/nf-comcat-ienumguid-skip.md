---
UID: NF:comcat.IEnumGUID.Skip
title: IEnumGUID::Skip (comcat.h)
description: Skips over the specified number of items in the enumeration sequence. (IEnumGUID.Skip)
helpviewer_keywords: ["IEnumGUID interface [COM]","Skip method","IEnumGUID.Skip","IEnumGUID::Skip","Skip","Skip method [COM]","Skip method [COM]","IEnumGUID interface","_com_ienumguid_skip","com.ienumguid_skip","comcat/IEnumGUID::Skip"]
old-location: com\ienumguid_skip.htm
tech.root: com
ms.assetid: 8c3b955b-ba36-4bab-af89-fc89e08e6e94
ms.date: 12/05/2018
ms.keywords: IEnumGUID interface [COM],Skip method, IEnumGUID.Skip, IEnumGUID::Skip, Skip, Skip method [COM], Skip method [COM],IEnumGUID interface, _com_ienumguid_skip, com.ienumguid_skip, comcat/IEnumGUID::Skip
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - IEnumGUID::Skip
 - comcat/IEnumGUID::Skip
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
 - IEnumGUID.Skip
---

# IEnumGUID::Skip


## -description

Skips over the specified number of items in the enumeration sequence.

## -parameters

### -param celt [in]

The number of items to be skipped.

## -returns

If the method skips the number of items requested, the return value is S_OK. Otherwise, it is S_FALSE.

## -see-also

<a href="/windows/desktop/api/comcat/nn-comcat-ienumguid">IEnumGUID</a>
