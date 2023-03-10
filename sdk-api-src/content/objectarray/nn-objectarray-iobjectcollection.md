---
UID: NN:objectarray.IObjectCollection
title: IObjectCollection (objectarray.h)
description: Extends the IObjectArray interface by providing methods that enable clients to add and remove objects that support IUnknown in a collection.
helpviewer_keywords: ["IObjectCollection","IObjectCollection interface [Windows Shell]","IObjectCollection interface [Windows Shell]","described","_shell_IObjectCollection","objectarray/IObjectCollection","shell.IObjectCollection"]
old-location: shell\IObjectCollection.htm
tech.root: shell
ms.assetid: d7665b26-5839-4b08-a099-ef25a68c65db
ms.date: 12/05/2018
ms.keywords: IObjectCollection, IObjectCollection interface [Windows Shell], IObjectCollection interface [Windows Shell],described, _shell_IObjectCollection, objectarray/IObjectCollection, shell.IObjectCollection
req.header: objectarray.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - IObjectCollection
 - objectarray/IObjectCollection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objectarray.h
api_name:
 - IObjectCollection
---

# IObjectCollection interface


## -description

Extends the <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a> interface by providing methods that enable clients to add and remove objects that support <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> in a collection.

## -inheritance

The <b>IObjectCollection</b> interface inherits from <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a>. <b>IObjectCollection</b> also has these types of members:

## -remarks

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to interact with a collection of generic objects.
