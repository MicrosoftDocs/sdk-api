---
UID: NF:d2d1_1.ID2D1Multithread.GetMultithreadProtected
title: ID2D1Multithread::GetMultithreadProtected (d2d1_1.h)
description: Returns whether the Direct2D factory was created with the D2D1_FACTORY_TYPE_MULTI_THREADED flag.
helpviewer_keywords: ["GetMultithreadProtected","GetMultithreadProtected method [Direct2D]","GetMultithreadProtected method [Direct2D]","ID2D1Multithread interface","ID2D1Multithread interface [Direct2D]","GetMultithreadProtected method","ID2D1Multithread.GetMultithreadProtected","ID2D1Multithread::GetMultithreadProtected","d2d1_1/ID2D1Multithread::GetMultithreadProtected","direct2d.id2d1multithread_getmultithreadprotected"]
old-location: direct2d\id2d1multithread_getmultithreadprotected.htm
tech.root: Direct2D
ms.assetid: C805B8C1-942B-4E56-97F2-756B0DD800A2
ms.date: 12/05/2018
ms.keywords: GetMultithreadProtected, GetMultithreadProtected method [Direct2D], GetMultithreadProtected method [Direct2D],ID2D1Multithread interface, ID2D1Multithread interface [Direct2D],GetMultithreadProtected method, ID2D1Multithread.GetMultithreadProtected, ID2D1Multithread::GetMultithreadProtected, d2d1_1/ID2D1Multithread::GetMultithreadProtected, direct2d.id2d1multithread_getmultithreadprotected
req.header: d2d1_1.h
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Multithread::GetMultithreadProtected
 - d2d1_1/ID2D1Multithread::GetMultithreadProtected
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.dll
api_name:
 - ID2D1Multithread.GetMultithreadProtected
---

# ID2D1Multithread::GetMultithreadProtected


## -description

Returns whether the Direct2D factory was created with the <a href="/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type">D2D1_FACTORY_TYPE_MULTI_THREADED</a> flag.



## -returns

Returns true if the Direct2D factory was created as multi-threaded, or false if it was created as single-threaded.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1multithread">ID2D1Multithread</a>
