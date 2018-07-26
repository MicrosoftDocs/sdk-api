---
UID: NF:objectarray.IObjectCollection.RemoveObjectAt
title: IObjectCollection::RemoveObjectAt
author: windows-sdk-content
description: Removes a single, specified object from the collection.
old-location: shell\IObjectCollection_RemoveObjectAt.htm
old-project: shell
ms.assetid: a0e526c0-a374-4952-8fe1-2a5aa53d9c41
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IObjectCollection interface [Windows Shell],RemoveObjectAt method, IObjectCollection.RemoveObjectAt, IObjectCollection::RemoveObjectAt, RemoveObjectAt, RemoveObjectAt method [Windows Shell], RemoveObjectAt method [Windows Shell],IObjectCollection interface, _shell_IObjectCollection_RemoveObjectAt, objectarray/IObjectCollection::RemoveObjectAt, shell.IObjectCollection_RemoveObjectAt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: COMSD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objectarray.h
api_name:
 - IObjectCollection.RemoveObjectAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



