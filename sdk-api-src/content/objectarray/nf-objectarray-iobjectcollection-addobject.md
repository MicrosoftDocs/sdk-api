---
UID: NF:objectarray.IObjectCollection.AddObject
title: IObjectCollection::AddObject
author: windows-driver-content
description: Adds a single object to the collection.
old-location: shell\IObjectCollection_AddObject.htm
old-project: shell
ms.assetid: 0898160d-46e5-4b38-9fc9-f74bd6a0385b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: AddObject, AddObject method [Windows Shell], AddObject method [Windows Shell],IObjectCollection interface, IObjectCollection interface [Windows Shell],AddObject method, IObjectCollection.AddObject, IObjectCollection::AddObject, _shell_IObjectCollection_AddObject, objectarray/IObjectCollection::AddObject, shell.IObjectCollection_AddObject
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
req.typenames: COMSD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objectarray.h
api_name:
-	IObjectCollection.AddObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IObjectCollection::AddObject


## -description


Adds a single object to the collection.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of the object to be added to the collection.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



