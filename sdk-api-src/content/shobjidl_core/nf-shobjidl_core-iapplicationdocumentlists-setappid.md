---
UID: NF:shobjidl_core.IApplicationDocumentLists.SetAppID
title: IApplicationDocumentLists::SetAppID (shobjidl_core.h)
description: Specifies a unique Application User Model ID (AppUserModelID) for the application whose destination lists are being retrieved. This method is optional.
helpviewer_keywords: ["IApplicationDocumentLists interface [Windows Shell]","SetAppID method","IApplicationDocumentLists.SetAppID","IApplicationDocumentLists::SetAppID","SetAppID","SetAppID method [Windows Shell]","SetAppID method [Windows Shell]","IApplicationDocumentLists interface","_shell_IApplicationDocumentLists_SetAppID","shell.IApplicationDocumentLists_SetAppID","shobjidl_core/IApplicationDocumentLists::SetAppID"]
old-location: shell\IApplicationDocumentLists_SetAppID.htm
tech.root: shell
ms.assetid: 1c5135c1-b98d-4d27-8437-5ca57af9a525
ms.date: 12/05/2018
ms.keywords: IApplicationDocumentLists interface [Windows Shell],SetAppID method, IApplicationDocumentLists.SetAppID, IApplicationDocumentLists::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],IApplicationDocumentLists interface, _shell_IApplicationDocumentLists_SetAppID, shell.IApplicationDocumentLists_SetAppID, shobjidl_core/IApplicationDocumentLists::SetAppID
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDocumentLists::SetAppID
 - shobjidl_core/IApplicationDocumentLists::SetAppID
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
 - IApplicationDocumentLists.SetAppID
---

# IApplicationDocumentLists::SetAppID


## -description

Specifies a unique Application User Model ID (AppUserModelID) for the application whose destination lists are being retrieved. This method is optional.

## -parameters

### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process whose taskbar button representation receives the Jump List.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the application has an explicit AppUserModelID, this method must be called before you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist">GetList</a>.

After an AppUserModelID is specified through an object's <b>SetAppID</b> method, the AppUserModelID is saved in the object for that object's lifetime, providing that it is not overwritten by another call to <b>SetAppID</b>.

Some applications will not declare an explicit AppUserModelID and should not call this method. In that case, the application's identity is deduced when <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist">IApplicationDocumentLists::GetList</a> is called. However, there is a performance benefit in avoiding those calculations, so applications that provide custom Jump Lists are encouraged to use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid">explicit AppUserModelIDs</a>.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists">IApplicationDocumentLists</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>