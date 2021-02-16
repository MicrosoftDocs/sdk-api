---
UID: NF:shobjidl_core.IShellLinkDataList.RemoveDataBlock
title: IShellLinkDataList::RemoveDataBlock (shobjidl_core.h)
description: Removes a data block from a link.
helpviewer_keywords: ["IShellLinkDataList interface [Windows Shell]","RemoveDataBlock method","IShellLinkDataList.RemoveDataBlock","IShellLinkDataList::RemoveDataBlock","RemoveDataBlock","RemoveDataBlock method [Windows Shell]","RemoveDataBlock method [Windows Shell]","IShellLinkDataList interface","_win32_IShellLinkDataList_RemoveDataBlock","shell.IShellLinkDataList_RemoveDataBlock","shobjidl_core/IShellLinkDataList::RemoveDataBlock"]
old-location: shell\IShellLinkDataList_RemoveDataBlock.htm
tech.root: shell
ms.assetid: 32660c95-4b09-4ede-b02d-bf3a335a9097
ms.date: 12/05/2018
ms.keywords: IShellLinkDataList interface [Windows Shell],RemoveDataBlock method, IShellLinkDataList.RemoveDataBlock, IShellLinkDataList::RemoveDataBlock, RemoveDataBlock, RemoveDataBlock method [Windows Shell], RemoveDataBlock method [Windows Shell],IShellLinkDataList interface, _win32_IShellLinkDataList_RemoveDataBlock, shell.IShellLinkDataList_RemoveDataBlock, shobjidl_core/IShellLinkDataList::RemoveDataBlock
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
 - IShellLinkDataList::RemoveDataBlock
 - shobjidl_core/IShellLinkDataList::RemoveDataBlock
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
 - IShellLinkDataList.RemoveDataBlock
---

# IShellLinkDataList::RemoveDataBlock


## -description

Removes a data block from a link.

## -parameters

### -param dwSig [in]

Type: <b>DWORD</b>

The data block's signature. The signature value for a particular type of data block can be found in its structure reference. For a list of supported data block types and their associated structures, see <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>