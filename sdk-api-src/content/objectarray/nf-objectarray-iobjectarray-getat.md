---
UID: NF:objectarray.IObjectArray.GetAt
title: IObjectArray::GetAt (objectarray.h)
description: Provides a pointer to a specified object's interface. The object and interface are specified by index and interface ID.
helpviewer_keywords: ["GetAt","GetAt method [Windows Shell]","GetAt method [Windows Shell]","IObjectArray interface","IObjectArray interface [Windows Shell]","GetAt method","IObjectArray.GetAt","IObjectArray::GetAt","_shell_IObjectArray_GetAt","objectarray/IObjectArray::GetAt","shell.IObjectArray_GetAt"]
old-location: shell\IObjectArray_GetAt.htm
tech.root: shell
ms.assetid: 168d2f09-60c9-457a-b4dd-7678f97eda1b
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [Windows Shell], GetAt method [Windows Shell],IObjectArray interface, IObjectArray interface [Windows Shell],GetAt method, IObjectArray.GetAt, IObjectArray::GetAt, _shell_IObjectArray_GetAt, objectarray/IObjectArray::GetAt, shell.IObjectArray_GetAt
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
 - IObjectArray::GetAt
 - objectarray/IObjectArray::GetAt
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
 - IObjectArray.GetAt
---

# IObjectArray::GetAt


## -description

Provides a pointer to a specified object's interface. The object and interface are specified by index and interface ID.

## -parameters

### -param uiIndex [in]

Type: <b>UINT</b>

The index of the object

### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired interface ID.

### -param ppv [out]

Type: <b>void**</b>

Receives the interface pointer requested in <i>riid</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

