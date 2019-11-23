---
UID: NF:shobjidl_core.IEnumAssocHandlers.Next
title: IEnumAssocHandlers::Next (shobjidl_core.h)

description: Retrieves a specified number of elements.
old-location: shell\IEnumAssocHandlers_Next.htm
tech.root: shell
ms.assetid: 9e173cb3-bd73-437c-8853-c13c8b6f216f

ms.date: 12/05/2018
ms.keywords: IEnumAssocHandlers interface [Windows Shell],Next method, IEnumAssocHandlers.Next, IEnumAssocHandlers::Next, Next, Next method [Windows Shell], Next method [Windows Shell],IEnumAssocHandlers interface, _shell_IEnumAssocHandlers_Next, shell.IEnumAssocHandlers_Next, shobjidl_core/IEnumAssocHandlers::Next
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IEnumAssocHandlers.Next"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IEnumAssocHandlers.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumAssocHandlers::Next


## -description


Retrieves a specified number of elements.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

The number of elements to retrieve.


### -param rgelt [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a>**</b>

When this method returns, contains the address of an array of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iassochandler">IAssocHandler</a> pointers. Each <b>IAssocHandler</b> represents a single handler.


### -param pceltFetched [out]

Type: <b>ULONG*</b>

When this method returns, contains a pointer to the number of elements retrieved.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



