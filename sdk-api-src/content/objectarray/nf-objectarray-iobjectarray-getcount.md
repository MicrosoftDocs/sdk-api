---
UID: NF:objectarray.IObjectArray.GetCount
title: IObjectArray::GetCount
author: windows-sdk-content
description: Provides a count of the objects in the collection.
old-location: shell\IObjectArray_GetCount.htm
old-project: shell
ms.assetid: 2803d8b1-7fc2-499b-a16b-b82b420cba66
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],IObjectArray interface, IObjectArray interface [Windows Shell],GetCount method, IObjectArray.GetCount, IObjectArray::GetCount, _shell_IObjectArray_GetCount, objectarray/IObjectArray::GetCount, shell.IObjectArray_GetCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IObjectArray.GetCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: ADAM
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



