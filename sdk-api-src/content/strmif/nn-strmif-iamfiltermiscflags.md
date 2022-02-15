---
UID: NN:strmif.IAMFilterMiscFlags
title: IAMFilterMiscFlags (strmif.h)
description: The IAMFilterMiscFlags interface queries whether a filter is a source filter or a renderer.
helpviewer_keywords: ["IAMFilterMiscFlags","IAMFilterMiscFlags interface [DirectShow]","IAMFilterMiscFlags interface [DirectShow]","described","IAMFilterMiscFlagsInterface","dshow.iamfiltermiscflags","strmif/IAMFilterMiscFlags"]
old-location: dshow\iamfiltermiscflags.htm
tech.root: dshow
ms.assetid: f9f3eaf9-4afa-412f-aa8f-b75e787cfecb
ms.date: 12/05/2018
ms.keywords: IAMFilterMiscFlags, IAMFilterMiscFlags interface [DirectShow], IAMFilterMiscFlags interface [DirectShow],described, IAMFilterMiscFlagsInterface, dshow.iamfiltermiscflags, strmif/IAMFilterMiscFlags
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMFilterMiscFlags
 - strmif/IAMFilterMiscFlags
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
 - IAMFilterMiscFlags
---

# IAMFilterMiscFlags interface


## -description

The <code>IAMFilterMiscFlags</code> interface queries whether a filter is a source filter or a renderer. Source and renderer filters should implement this interface.

Applications do not use this interface. The Filter Graph Manager uses this interface to determine how many <a href="/windows/desktop/DirectShow/ec-complete">EC_COMPLETE</a> events it will receive when playback completes.

## -inheritance

The <b>IAMFilterMiscFlags</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMFilterMiscFlags</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
