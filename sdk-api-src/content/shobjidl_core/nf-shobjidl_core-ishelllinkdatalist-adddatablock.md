---
UID: NF:shobjidl_core.IShellLinkDataList.AddDataBlock
title: IShellLinkDataList::AddDataBlock (shobjidl_core.h)
description: Adds a data block to a link.
helpviewer_keywords: ["AddDataBlock","AddDataBlock method [Windows Shell]","AddDataBlock method [Windows Shell]","IShellLinkDataList interface","IShellLinkDataList interface [Windows Shell]","AddDataBlock method","IShellLinkDataList.AddDataBlock","IShellLinkDataList::AddDataBlock","_win32_IShellLinkDataList_AddDataBlock","shell.IShellLinkDataList_AddDataBlock","shobjidl_core/IShellLinkDataList::AddDataBlock"]
old-location: shell\IShellLinkDataList_AddDataBlock.htm
tech.root: shell
ms.assetid: 6580736f-e217-4e3e-9b6e-1c1c004916f4
ms.date: 12/05/2018
ms.keywords: AddDataBlock, AddDataBlock method [Windows Shell], AddDataBlock method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],AddDataBlock method, IShellLinkDataList.AddDataBlock, IShellLinkDataList::AddDataBlock, _win32_IShellLinkDataList_AddDataBlock, shell.IShellLinkDataList_AddDataBlock, shobjidl_core/IShellLinkDataList::AddDataBlock
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkDataList::AddDataBlock
 - shobjidl_core/IShellLinkDataList::AddDataBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLinkDataList.AddDataBlock
---

# IShellLinkDataList::AddDataBlock


## -description

Adds a data block to a link.

## -parameters

### -param pDataBlock [in]

Type: <b>VOID*</b>

The data block structure. For a list of supported structures, see <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>