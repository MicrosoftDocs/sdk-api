---
UID: NF:shobjidl_core.IEnumFullIDList.Clone
title: IEnumFullIDList::Clone (shobjidl_core.h)
author: windows-sdk-content
description: Creates a new item enumeration object with the same contents and state as the current one.
old-location: shell\IEnumFullIDList_Clone.htm
tech.root: shell
ms.assetid: 23345978-6178-4f6d-8757-d5fd95199067
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Windows Shell], Clone method [Windows Shell],IEnumFullIDList interface, IEnumFullIDList interface [Windows Shell],Clone method, IEnumFullIDList.Clone, IEnumFullIDList::Clone, _shell_IEnumFullIDList_Clone, shell.IEnumFullIDList_Clone, shobjidl_core/IEnumFullIDList::Clone
ms.topic: method
f1_keywords: 
 - "shobjidl_core/IEnumFullIDList.Clone"
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
 - IEnumFullIDList.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumFullIDList::Clone


## -description


Creates a new item enumeration object with the same contents and state as the current one.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist">IEnumFullIDList</a>**</b>

On success, contains the address of an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumfullidlist">IEnumFullIDList</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



