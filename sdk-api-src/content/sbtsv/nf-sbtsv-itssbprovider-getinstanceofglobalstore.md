---
UID: NF:sbtsv.ITsSbProvider.GetInstanceOfGlobalStore
title: ITsSbProvider::GetInstanceOfGlobalStore (sbtsv.h)
description: Retrieves an ITsSbGlobalStore instance of the global store object.
helpviewer_keywords: ["GetInstanceOfGlobalStore","GetInstanceOfGlobalStore method [Remote Desktop Services]","GetInstanceOfGlobalStore method [Remote Desktop Services]","ITsSbProvider interface","ITsSbProvider interface [Remote Desktop Services]","GetInstanceOfGlobalStore method","ITsSbProvider.GetInstanceOfGlobalStore","ITsSbProvider::GetInstanceOfGlobalStore","sbtsv/ITsSbProvider::GetInstanceOfGlobalStore","termserv.itssbprovider_getinstanceofglobalstore"]
old-location: termserv\itssbprovider_getinstanceofglobalstore.htm
tech.root: TermServ
ms.assetid: e6c83775-56e7-4342-a26a-418f472e190f
ms.date: 12/05/2018
ms.keywords: GetInstanceOfGlobalStore, GetInstanceOfGlobalStore method [Remote Desktop Services], GetInstanceOfGlobalStore method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],GetInstanceOfGlobalStore method, ITsSbProvider.GetInstanceOfGlobalStore, ITsSbProvider::GetInstanceOfGlobalStore, sbtsv/ITsSbProvider::GetInstanceOfGlobalStore, termserv.itssbprovider_getinstanceofglobalstore
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbProvider::GetInstanceOfGlobalStore
 - sbtsv/ITsSbProvider::GetInstanceOfGlobalStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.GetInstanceOfGlobalStore
---

# ITsSbProvider::GetInstanceOfGlobalStore


## -description

Retrieves an <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a> instance of the global store object.

Plug-ins can use this method to get an instance of the global store object. The global store object is designed for use by filter plug-ins that do not have access to the resource plug-in store.

## -parameters

### -param ppGlobalStore [out]

A pointer to a pointer to a global store object. When you have finished using the object, release it by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore">ITsSbGlobalStore</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider">ITsSbProvider</a>