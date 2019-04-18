---
UID: NF:propsys.IDelayedPropertyStoreFactory.GetDelayedPropertyStore
title: IDelayedPropertyStoreFactory::GetDelayedPropertyStore (propsys.h)
author: windows-sdk-content
description: Gets an IPropertyStore interface object, as specified.
old-location: shell\IDelayedPropertyStoreFactory_GetDelayedPropertyStore.htm
tech.root: shell
ms.assetid: 26df5fec-2a21-454e-9539-877c00a4f8fb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDelayedPropertyStore, GetDelayedPropertyStore method [Windows Shell], GetDelayedPropertyStore method [Windows Shell],IDelayedPropertyStoreFactory interface, IDelayedPropertyStoreFactory interface [Windows Shell],GetDelayedPropertyStore method, IDelayedPropertyStoreFactory.GetDelayedPropertyStore, IDelayedPropertyStoreFactory::GetDelayedPropertyStore, STOREID_FALLBACK, STOREID_FILE, STOREID_INNATE, _shell_IDelayedPropertyStoreFactory_GetDelayedPropertyStore, propsys/IDelayedPropertyStoreFactory::GetDelayedPropertyStore, shell.IDelayedPropertyStoreFactory_GetDelayedPropertyStore
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IDelayedPropertyStoreFactory.GetDelayedPropertyStore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDelayedPropertyStoreFactory::GetDelayedPropertyStore


## -description


Gets an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface object, as specified.


## -parameters




### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a></b>

The GPS_XXX flags that modify the store that is returned. See <a href="https://msdn.microsoft.com/d3fde1b9-b19f-431d-9cea-bffc289ee683">GETPROPERTYSTOREFLAGS</a>.


### -param dwStoreId [in]

Type: <b>DWORD</b>

The property store ID. Valid values are.



#### STOREID_INNATE

Value is 0.



#### STOREID_FILE

Value is 1.



#### STOREID_FALLBACK

Value is 2.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired IID.


### -param ppv [out]

Type: <b>void**</b>

The address of an <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



