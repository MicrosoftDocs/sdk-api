---
UID: NF:shobjidl_core.IShellItemArray.GetCount
title: IShellItemArray::GetCount (shobjidl_core.h)
description: Gets the number of items in the given IShellItem array.
helpviewer_keywords: ["GetCount","GetCount method [Windows Shell]","GetCount method [Windows Shell]","IShellItemArray interface","IShellItemArray interface [Windows Shell]","GetCount method","IShellItemArray.GetCount","IShellItemArray::GetCount","_shell_IShellItemArray_GetCount","shell.IShellItemArray_GetCount","shobjidl_core/IShellItemArray::GetCount"]
old-location: shell\IShellItemArray_GetCount.htm
tech.root: shell
ms.assetid: 84d20695-bd51-4727-bd82-bd104de99067
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method [Windows Shell], GetCount method [Windows Shell],IShellItemArray interface, IShellItemArray interface [Windows Shell],GetCount method, IShellItemArray.GetCount, IShellItemArray::GetCount, _shell_IShellItemArray_GetCount, shell.IShellItemArray_GetCount, shobjidl_core/IShellItemArray::GetCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemArray::GetCount
 - shobjidl_core/IShellItemArray::GetCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray.GetCount
---

# IShellItemArray::GetCount


## -description

Gets the number of items in the given <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> array.

## -parameters

### -param pdwNumItems [out]

Type: <b>DWORD*</b>

When this method returns, contains the number of items in the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getitemat">IShellItemArray::GetItemAt</a>