---
UID: NN:d2d1effectauthor.ID2D1AnalysisTransform
title: ID2D1AnalysisTransform (d2d1effectauthor.h)
description: Supplies data to an analysis effect.
helpviewer_keywords: ["ID2D1AnalysisTransform","ID2D1AnalysisTransform interface [Direct2D]","ID2D1AnalysisTransform interface [Direct2D]","described","d2d1effectauthor/ID2D1AnalysisTransform","direct2d.id2d1analysistransform"]
old-location: direct2d\id2d1analysistransform.htm
tech.root: Direct2D
ms.assetid: 64CDA0A7-2790-436C-9EFC-3A74D09602B9
ms.date: 12/05/2018
ms.keywords: ID2D1AnalysisTransform, ID2D1AnalysisTransform interface [Direct2D], ID2D1AnalysisTransform interface [Direct2D],described, d2d1effectauthor/ID2D1AnalysisTransform, direct2d.id2d1analysistransform
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1AnalysisTransform
 - d2d1effectauthor/ID2D1AnalysisTransform
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1AnalysisTransform
---

# ID2D1AnalysisTransform interface


## -description

Supplies data to an analysis effect.

## -inheritance

The <b>ID2D1AnalysisTransform</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1AnalysisTransform</b> also has these types of members:

## -remarks

This interface can be implemented by an <a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1computetransform">ID2D1ComputeTransform</a>. The analysis transform must be the output node of an effect's transform graph, and the effect's registration XML must include the `type="Analysis"` attribute on the root `<Effect>` node.
