---
UID: NF:objectarray.IObjectCollection.RemoveObjectAt
title: IObjectCollection::RemoveObjectAt (objectarray.h)
description: Removes a single, specified object from the collection.
helpviewer_keywords: ["IObjectCollection interface [Windows Shell]","RemoveObjectAt method","IObjectCollection.RemoveObjectAt","IObjectCollection::RemoveObjectAt","RemoveObjectAt","RemoveObjectAt method [Windows Shell]","RemoveObjectAt method [Windows Shell]","IObjectCollection interface","_shell_IObjectCollection_RemoveObjectAt","objectarray/IObjectCollection::RemoveObjectAt","shell.IObjectCollection_RemoveObjectAt"]
old-location: shell\IObjectCollection_RemoveObjectAt.htm
tech.root: shell
ms.assetid: a0e526c0-a374-4952-8fe1-2a5aa53d9c41
ms.date: 12/05/2018
ms.keywords: IObjectCollection interface [Windows Shell],RemoveObjectAt method, IObjectCollection.RemoveObjectAt, IObjectCollection::RemoveObjectAt, RemoveObjectAt, RemoveObjectAt method [Windows Shell], RemoveObjectAt method [Windows Shell],IObjectCollection interface, _shell_IObjectCollection_RemoveObjectAt, objectarray/IObjectCollection::RemoveObjectAt, shell.IObjectCollection_RemoveObjectAt
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
 - IObjectCollection::RemoveObjectAt
 - objectarray/IObjectCollection::RemoveObjectAt
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
 - IObjectCollection.RemoveObjectAt
---

# IObjectCollection::RemoveObjectAt


## -description

Removes a single, specified object from the collection.

## -parameters

### -param uiIndex [in]

Type: <b>UINT*</b>

A pointer to the index of the object within the collection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

