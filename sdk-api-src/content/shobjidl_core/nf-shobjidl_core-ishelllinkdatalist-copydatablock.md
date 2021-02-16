---
UID: NF:shobjidl_core.IShellLinkDataList.CopyDataBlock
title: IShellLinkDataList::CopyDataBlock (shobjidl_core.h)
description: Retrieves a copy of a link's data block.
helpviewer_keywords: ["CopyDataBlock","CopyDataBlock method [Windows Shell]","CopyDataBlock method [Windows Shell]","IShellLinkDataList interface","IShellLinkDataList interface [Windows Shell]","CopyDataBlock method","IShellLinkDataList.CopyDataBlock","IShellLinkDataList::CopyDataBlock","_win32_IShellLinkDataList_CopyDataBlock","shell.IShellLinkDataList_CopyDataBlock","shobjidl_core/IShellLinkDataList::CopyDataBlock"]
old-location: shell\IShellLinkDataList_CopyDataBlock.htm
tech.root: shell
ms.assetid: e02fb4c3-faec-40cc-ab97-d05cdcc148ed
ms.date: 12/05/2018
ms.keywords: CopyDataBlock, CopyDataBlock method [Windows Shell], CopyDataBlock method [Windows Shell],IShellLinkDataList interface, IShellLinkDataList interface [Windows Shell],CopyDataBlock method, IShellLinkDataList.CopyDataBlock, IShellLinkDataList::CopyDataBlock, _win32_IShellLinkDataList_CopyDataBlock, shell.IShellLinkDataList_CopyDataBlock, shobjidl_core/IShellLinkDataList::CopyDataBlock
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
 - IShellLinkDataList::CopyDataBlock
 - shobjidl_core/IShellLinkDataList::CopyDataBlock
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
 - IShellLinkDataList.CopyDataBlock
---

# IShellLinkDataList::CopyDataBlock


## -description

Retrieves a copy of a link's data block.

## -parameters

### -param dwSig [in]

Type: <b>DWORD</b>

The data block's signature. The signature value for a particular type of data block can be found in its structure reference. For a list of supported data block types and their associated structures, see <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>.

### -param ppDataBlock [out]

Type: <b>VOID**</b>

The address of a pointer to a copy of the data block structure. If <b>IShellLinkDataList::CopyDataBlock</b> returns a successful result, the calling application must free the memory when it is no longer needed by calling <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>