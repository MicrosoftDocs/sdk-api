---
UID: NF:shobjidl_core.ICustomDestinationList.SetAppID
title: ICustomDestinationList::SetAppID (shobjidl_core.h)
description: Specifies a unique Application User Model ID (AppUserModelID) for the application whose taskbar button will hold the custom Jump List built through the methods of this interface. This method is optional.
helpviewer_keywords: ["ICustomDestinationList interface [Windows Shell]","SetAppID method","ICustomDestinationList.SetAppID","ICustomDestinationList::SetAppID","SetAppID","SetAppID method [Windows Shell]","SetAppID method [Windows Shell]","ICustomDestinationList interface","_shell_ICustomDestinationList_SetAppID","shell.ICustomDestinationList_SetAppID","shobjidl_core/ICustomDestinationList::SetAppID"]
old-location: shell\ICustomDestinationList_SetAppID.htm
tech.root: shell
ms.assetid: 7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd
ms.date: 12/05/2018
ms.keywords: ICustomDestinationList interface [Windows Shell],SetAppID method, ICustomDestinationList.SetAppID, ICustomDestinationList::SetAppID, SetAppID, SetAppID method [Windows Shell], SetAppID method [Windows Shell],ICustomDestinationList interface, _shell_ICustomDestinationList_SetAppID, shell.ICustomDestinationList_SetAppID, shobjidl_core/ICustomDestinationList::SetAppID
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
 - ICustomDestinationList::SetAppID
 - shobjidl_core/ICustomDestinationList::SetAppID
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
 - ICustomDestinationList.SetAppID
---

# ICustomDestinationList::SetAppID


## -description

Specifies a unique Application User Model ID (AppUserModelID) for the application whose taskbar button will hold the custom Jump List built through the methods of this interface. This method is optional.

## -parameters

### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process or application whose taskbar representation receives the Jump List.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This method was called after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a>. The list-building process is already running with a particular AppUserModelID, either inferred by the system or set through a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid">SetAppID</a> before the call to <b>BeginList</b>. After a list-building operation is in progress, the AppUserModelID cannot be changed until after <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-commitlist">CommitList</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-abortlist">AbortList</a> has been called.

</td>
</tr>
</table>

## -remarks

If an application has an explicit AppUserModelID, you must call <b>SetAppID</b> before you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-getremoveddestinations">ICustomDestinationList::GetRemovedDestinations</a>.

After an AppUserModelID is specified through an object's <b>SetAppID</b> method, the AppUserModelID is saved in the object for that object's lifetime, providing that it is not overwritten by another call to <b>SetAppID</b>.

Some applications will not declare an explicit AppUserModelID and should not call this method. In that case, the application's identity is deduced when <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-getremoveddestinations">ICustomDestinationList::GetRemovedDestinations</a> are called. However, there is a performance benefit in avoiding those calculations, so applications that provide custom Jump Lists are encouraged to use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid">explicit AppUserModelIDs</a>.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid">SetCurrentProcessExplicitAppUserModelID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>