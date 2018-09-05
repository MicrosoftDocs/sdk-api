---
UID: NF:objectarray.IObjectArray.GetAt
title: IObjectArray::GetAt
author: windows-sdk-content
description: Provides a pointer to a specified object's interface. The object and interface are specified by index and interface ID.
old-location: shell\IObjectArray_GetAt.htm
old-project: shell
ms.assetid: 168d2f09-60c9-457a-b4dd-7678f97eda1b
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetAt, GetAt method [Windows Shell], GetAt method [Windows Shell],IObjectArray interface, IObjectArray interface [Windows Shell],GetAt method, IObjectArray.GetAt, IObjectArray::GetAt, _shell_IObjectArray_GetAt, objectarray/IObjectArray::GetAt, shell.IObjectArray_GetAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objectarray.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IObjectArray.GetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



