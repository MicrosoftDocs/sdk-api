---
UID: NN:objidl.ILayoutStorage
title: ILayoutStorage (objidl.h)
description: The ILayoutStorage interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link.
helpviewer_keywords: ["ILayoutStorage","ILayoutStorage interface [Structured Storage]","ILayoutStorage interface [Structured Storage]","described","_stg_ilayoutstorage","objidl/ILayoutStorage","stg.ilayoutstorage"]
old-location: stg\ilayoutstorage.htm
tech.root: Stg
ms.assetid: 72201600-4bbb-4346-a13f-927e8463b6ec
ms.date: 12/05/2018
ms.keywords: ILayoutStorage, ILayoutStorage interface [Structured Storage], ILayoutStorage interface [Structured Storage],described, _stg_ilayoutstorage, objidl/ILayoutStorage, stg.ilayoutstorage
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILayoutStorage
 - objidl/ILayoutStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - ILayoutStorage
---

# ILayoutStorage interface


## -description

The 
<b>ILayoutStorage</b> interface enables an application to optimize the layout of its compound files for efficient downloading across a slow link. The goal is to enable a browser or other application to download data in the order in which it will actually be required.

To optimize a compound file, an application  calls <a href="/windows/desktop/api/objidl/nf-objidl-istorage-copyto">CopyTo</a>  to layout a docfile, thus improving performance in most scenarios.

## -inheritance

The <b>ILayoutStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILayoutStorage</b> also has these types of members:

