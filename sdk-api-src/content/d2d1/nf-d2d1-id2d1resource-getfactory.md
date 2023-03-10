---
UID: NF:d2d1.ID2D1Resource.GetFactory
title: ID2D1Resource::GetFactory (d2d1.h)
description: Retrieves the factory associated with this resource.
helpviewer_keywords: ["GetFactory","GetFactory method [Direct2D]","GetFactory method [Direct2D]","ID2D1Resource interface","ID2D1Resource interface [Direct2D]","GetFactory method","ID2D1Resource.GetFactory","ID2D1Resource::GetFactory","d2d1/ID2D1Resource::GetFactory","direct2d.ID2D1Resource_GetFactory"]
old-location: direct2d\ID2D1Resource_GetFactory.htm
tech.root: Direct2D
ms.assetid: 93afc187-d1ef-46f8-98b0-efe31345ae98
ms.date: 12/05/2018
ms.keywords: GetFactory, GetFactory method [Direct2D], GetFactory method [Direct2D],ID2D1Resource interface, ID2D1Resource interface [Direct2D],GetFactory method, ID2D1Resource.GetFactory, ID2D1Resource::GetFactory, d2d1/ID2D1Resource::GetFactory, direct2d.ID2D1Resource_GetFactory
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
 - ID2D1Resource::GetFactory
 - d2d1/ID2D1Resource::GetFactory
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
 - ID2D1Resource.GetFactory
---

# ID2D1Resource::GetFactory


## -description

Retrieves the factory associated with this resource.

## -parameters

### -param factory [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>**</b>

When this method returns, contains a pointer to a pointer to the factory that created this resource. This parameter is passed uninitialized.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

