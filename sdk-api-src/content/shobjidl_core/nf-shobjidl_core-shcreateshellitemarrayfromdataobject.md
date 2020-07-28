---
UID: NF:shobjidl_core.SHCreateShellItemArrayFromDataObject
title: SHCreateShellItemArrayFromDataObject function (shobjidl_core.h)
description: Creates a Shell item array object from a data object.
helpviewer_keywords: ["SHCreateShellItemArrayFromDataObject","SHCreateShellItemArrayFromDataObject function [Windows Shell]","_shell_SHCreateShellItemArrayFromDataObject","shell.SHCreateShellItemArrayFromDataObject","shobjidl_core/SHCreateShellItemArrayFromDataObject"]
old-location: shell\SHCreateShellItemArrayFromDataObject.htm
tech.root: shell
ms.assetid: 91e65c9a-0600-42e3-97f5-2a5960e1ec89
ms.date: 12/05/2018
ms.keywords: SHCreateShellItemArrayFromDataObject, SHCreateShellItemArrayFromDataObject function [Windows Shell], _shell_SHCreateShellItemArrayFromDataObject, shell.SHCreateShellItemArrayFromDataObject, shobjidl_core/SHCreateShellItemArrayFromDataObject
f1_keywords:
- shobjidl_core/SHCreateShellItemArrayFromDataObject
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
api_name:
- SHCreateShellItemArrayFromDataObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHCreateShellItemArrayFromDataObject function


## -description


Creates a Shell item array object from a data object. 


## -parameters




### -param pdo [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the desired interface ID.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is usefull for Shell extensions that implement <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellextinit">IShellExtInit</a> and are passed a data object to the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize">IShellExtInit::Initialize</a> method; for example, context menu handlers.

This API lets you convert the data object into a Shell item that the handler can consume. It is recommend that handlers use a Shell item array rather than clipboard formats like <b>CF_HDROP</b> and <b>CFSTR_SHELLIDLIST</b> (also known as HIDA) as it leads to simpler code and allows some performance improvements.

The resulting shell item array holds a reference to the source data object.  Therefore, that data object must remain valid for the lifetime of the shell item array.  Notably, the data objects passed to <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-idroptarget">IDropTarget</a> methods are no longer valid after the drop operation completes.



