---
UID: NF:objectarray.IObjectCollection.AddFromArray
title: IObjectCollection::AddFromArray
author: windows-sdk-content
description: Adds the objects contained in an IObjectArray to the collection.
old-location: shell\IObjectCollection_AddFromArray.htm
tech.root: shell
ms.assetid: fc51b2e0-a5e0-4440-a279-e94640b5dda7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AddFromArray, AddFromArray method [Windows Shell], AddFromArray method [Windows Shell],IObjectCollection interface, IObjectCollection interface [Windows Shell],AddFromArray method, IObjectCollection.AddFromArray, IObjectCollection::AddFromArray, _shell_IObjectCollection_AddFromArray, objectarray/IObjectCollection::AddFromArray, shell.IObjectCollection_AddFromArray
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objectarray.h
api_name:
 - IObjectCollection.AddFromArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IObjectCollection::AddFromArray


## -description


Adds the objects contained in an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> to the collection.


## -parameters




### -param poaSource [in]

Type: <b><a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> whose contents are to be added to the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



