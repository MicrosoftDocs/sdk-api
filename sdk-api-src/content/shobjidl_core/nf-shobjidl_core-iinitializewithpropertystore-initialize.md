---
UID: NF:shobjidl_core.IInitializeWithPropertyStore.Initialize
title: IInitializeWithPropertyStore::Initialize (shobjidl_core.h)
description: Initializes a handler with an IPropertyStore.helpviewer_keywords: ["IInitializeWithPropertyStore interface [Windows Shell]","Initialize method","IInitializeWithPropertyStore.Initialize","IInitializeWithPropertyStore::Initialize","Initialize","Initialize method [Windows Shell]","Initialize method [Windows Shell]","IInitializeWithPropertyStore interface","_shell_IInitializeWithPropertyStore_Initialize","shell.IInitializeWithPropertyStore_Initialize","shobjidl_core/IInitializeWithPropertyStore::Initialize"]
old-location: shell\IInitializeWithPropertyStore_Initialize.htm
tech.root: shell
ms.assetid: 6890873f-d929-42a1-ab75-6f408581d74f
ms.date: 12/05/2018
ms.keywords: IInitializeWithPropertyStore interface [Windows Shell],Initialize method, IInitializeWithPropertyStore.Initialize, IInitializeWithPropertyStore::Initialize, Initialize, Initialize method [Windows Shell], Initialize method [Windows Shell],IInitializeWithPropertyStore interface, _shell_IInitializeWithPropertyStore_Initialize, shell.IInitializeWithPropertyStore_Initialize, shobjidl_core/IInitializeWithPropertyStore::Initialize
f1_keywords:
- shobjidl_core/IInitializeWithPropertyStore.Initialize
dev_langs:
- c++
req.header: shobjidl_core.h
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
- shobjidl_core.h
api_name:
- IInitializeWithPropertyStore.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInitializeWithPropertyStore::Initialize


## -description


Initializes a handler with an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.


## -parameters




### -param pps [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method supports initializing handlers for use with OpenSearch result sets, which are returned from web services as RSS or Atom feeds.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializewithpropertystore">IInitializeWithPropertyStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a>
 

 

