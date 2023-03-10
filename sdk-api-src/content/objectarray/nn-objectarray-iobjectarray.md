---
UID: NN:objectarray.IObjectArray
title: IObjectArray (objectarray.h)
description: Exposes methods that enable clients to access items in a collection of objects that support IUnknown.
helpviewer_keywords: ["IObjectArray","IObjectArray interface [Windows Shell]","IObjectArray interface [Windows Shell]","described","_shell_IObjectArray","objectarray/IObjectArray","shell.IObjectArray"]
old-location: shell\IObjectArray.htm
tech.root: shell
ms.assetid: ab0bb213-dc9c-4853-98d7-668e7ca76583
ms.date: 12/05/2018
ms.keywords: IObjectArray, IObjectArray interface [Windows Shell], IObjectArray interface [Windows Shell],described, _shell_IObjectArray, objectarray/IObjectArray, shell.IObjectArray
req.header: objectarray.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objectarray.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IObjectArray
 - objectarray/IObjectArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IObjectArray
---

# IObjectArray interface


## -description

Exposes methods that enable clients to access items in a collection of objects that support <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>.

## -inheritance

The <b>IObjectArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectArray</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Clients do not need to implement this interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use this interface to access generic objects in an array.
