---
UID: NF:d2d1.ID2D1SimplifiedGeometrySink.SetSegmentFlags
title: ID2D1SimplifiedGeometrySink::SetSegmentFlags (d2d1.h)
description: Specifies stroke and join options to be applied to new segments added to the geometry sink.
helpviewer_keywords: ["ID2D1SimplifiedGeometrySink interface [Direct2D]","SetSegmentFlags method","ID2D1SimplifiedGeometrySink.SetSegmentFlags","ID2D1SimplifiedGeometrySink::SetSegmentFlags","SetSegmentFlags","SetSegmentFlags method [Direct2D]","SetSegmentFlags method [Direct2D]","ID2D1SimplifiedGeometrySink interface","d2d1/ID2D1SimplifiedGeometrySink::SetSegmentFlags","direct2d.ID2D1SimplifiedGeometrySink_SetSegmentFlags"]
old-location: direct2d\ID2D1SimplifiedGeometrySink_SetSegmentFlags.htm
tech.root: Direct2D
ms.assetid: e1162564-a39b-4c16-887e-ec06dd37301c
ms.date: 12/05/2018
ms.keywords: ID2D1SimplifiedGeometrySink interface [Direct2D],SetSegmentFlags method, ID2D1SimplifiedGeometrySink.SetSegmentFlags, ID2D1SimplifiedGeometrySink::SetSegmentFlags, SetSegmentFlags, SetSegmentFlags method [Direct2D], SetSegmentFlags method [Direct2D],ID2D1SimplifiedGeometrySink interface, d2d1/ID2D1SimplifiedGeometrySink::SetSegmentFlags, direct2d.ID2D1SimplifiedGeometrySink_SetSegmentFlags
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1SimplifiedGeometrySink::SetSegmentFlags
 - d2d1/ID2D1SimplifiedGeometrySink::SetSegmentFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1SimplifiedGeometrySink.SetSegmentFlags
---

# ID2D1SimplifiedGeometrySink::SetSegmentFlags


## -description

Specifies stroke and join options to be applied to new segments added to the geometry sink.

## -parameters

### -param vertexFlags

Type: <b><a href="/windows/win32/api/d2d1/ne-d2d1-d2d1_path_segment">D2D1_PATH_SEGMENT</a></b>

Stroke and join options to be applied to new segments added to the geometry sink.

## -remarks

After this method is called, the specified segment flags are applied to each segment subsequently added to the sink. The segment flags are applied to every additional segment until this method is called again and a different set of segment flags is specified.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink">ID2D1SimplifiedGeometrySink</a>

