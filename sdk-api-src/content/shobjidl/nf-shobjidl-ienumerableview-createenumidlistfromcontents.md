---
UID: NF:shobjidl.IEnumerableView.CreateEnumIDListFromContents
title: IEnumerableView::CreateEnumIDListFromContents
author: windows-sdk-content
description: Creates an enumerator of ID lists from the contents of the view.
old-location: shell\IEnumerableView_CreateEnumIDListFromContents.htm
tech.root: shell
ms.assetid: 413d913d-e6f3-4e2d-bf1f-5d5ad6d4f650
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: CreateEnumIDListFromContents, CreateEnumIDListFromContents method [Windows Shell], CreateEnumIDListFromContents method [Windows Shell],IEnumerableView interface, IEnumerableView interface [Windows Shell],CreateEnumIDListFromContents method, IEnumerableView.CreateEnumIDListFromContents, IEnumerableView::CreateEnumIDListFromContents, _shell_IEnumerableView_CreateEnumIDListFromContents, shell.IEnumerableView_CreateEnumIDListFromContents, shobjidl/IEnumerableView::CreateEnumIDListFromContents
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
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
 - Shobjidl.h
api_name:
 - IEnumerableView.CreateEnumIDListFromContents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumerableView::CreateEnumIDListFromContents


## -description


Creates an enumerator of ID lists from the contents of the view.


## -parameters




### -param pidlFolder [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

A PIDL that is relative to the Desktop.


### -param dwEnumFlags [in]

Type: <b>DWORD</b>

Specifies enumeration flags. See the <a href="https://msdn.microsoft.com/a46845bf-ade6-4366-8a73-6dc960fd7722">SHCONTF</a> enumerated type.


### -param ppEnumIDList [out]

Type: <b><a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a>**</b>

When this method returns, contains an <a href="https://msdn.microsoft.com/b6f139d3-c54c-4350-9d8b-cd534909a488">IEnumIDList</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

Returns a success value if successful, or an error value otherwise.



