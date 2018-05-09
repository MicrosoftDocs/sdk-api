---
UID: NF:propsys.INamedPropertyStore.GetNameAt
title: INamedPropertyStore::GetNameAt
author: windows-driver-content
description: Gets the name of a property at a specified index in the property store.
old-location: shell\INamedPropertyStore_GetNameAt.htm
old-project: shell
ms.assetid: 2fd3896e-b170-49af-811e-a1f2facc7a84
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: GetNameAt, GetNameAt method [Windows Shell], GetNameAt method [Windows Shell],INamedPropertyStore interface, INamedPropertyStore interface [Windows Shell],GetNameAt method, INamedPropertyStore.GetNameAt, INamedPropertyStore::GetNameAt, _shell_INamedPropertyStore_GetNameAt, propsys/INamedPropertyStore::GetNameAt, shell.INamedPropertyStore_GetNameAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	INamedPropertyStore.GetNameAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# INamedPropertyStore::GetNameAt


## -description


Gets the name of a property at a specified index in the property store.


## -parameters




### -param iProp [in]

Type: <b>DWORD</b>

The index of the property in the store.


### -param pbstrName [out]

Type: <b><a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a>*</b>

When this method returns, contains a pointer to the property's name. It is the calling application's responsibility to free this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



