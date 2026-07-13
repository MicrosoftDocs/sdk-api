---
UID: NF:objectarray.IObjectArray.GetCount
title: IObjectArray::GetCount (objectarray.h)
description: Provides a count of the objects in the collection.
helpviewer_keywords: ["GetCount","GetCount method [Windows Shell]","GetCount method [Windows Shell]","IObjectArray interface","IObjectArray interface [Windows Shell]","GetCount method","IObjectArray.GetCount","IObjectArray::GetCount","_shell_IObjectArray_GetCount","objectarray/IObjectArray::GetCount","shell.IObjectArray_GetCount"]
old-location: shell\IObjectArray_GetCount.htm
tech.root: shell
ms.assetid: 2803d8b1-7fc2-499b-a16b-b82b420cba66
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],IObjectArray interface, IObjectArray interface [Windows Shell],GetCount method, IObjectArray.GetCount, IObjectArray::GetCount, _shell_IObjectArray_GetCount, objectarray/IObjectArray::GetCount, shell.IObjectArray_GetCount
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
 - IObjectArray::GetCount
 - objectarray/IObjectArray::GetCount
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
 - IObjectArray.GetCount
---

# IObjectArray::GetCount


## -description

Provides a count of the objects in the collection.

## -parameters

### -param pcObjects [out]

Type: <b>UINT*</b>

The number of objects in the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

