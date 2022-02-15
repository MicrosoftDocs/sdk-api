---
UID: NF:shobjidl_core.ICustomDestinationList.DeleteList
title: ICustomDestinationList::DeleteList (shobjidl_core.h)
description: Deletes a custom Jump List for a specified application.
helpviewer_keywords: ["DeleteList","DeleteList method [Windows Shell]","DeleteList method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","DeleteList method","ICustomDestinationList.DeleteList","ICustomDestinationList::DeleteList","_shell_ICustomDestinationList_DeleteList","shell.ICustomDestinationList_DeleteList","shobjidl_core/ICustomDestinationList::DeleteList"]
old-location: shell\ICustomDestinationList_DeleteList.htm
tech.root: shell
ms.assetid: ef246f5a-9fcf-4475-b19a-e676f0351f3f
ms.date: 12/05/2018
ms.keywords: DeleteList, DeleteList method [Windows Shell], DeleteList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],DeleteList method, ICustomDestinationList.DeleteList, ICustomDestinationList::DeleteList, _shell_ICustomDestinationList_DeleteList, shell.ICustomDestinationList_DeleteList, shobjidl_core/ICustomDestinationList::DeleteList
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
 - ICustomDestinationList::DeleteList
 - shobjidl_core/ICustomDestinationList::DeleteList
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
 - ICustomDestinationList.DeleteList
---

# ICustomDestinationList::DeleteList


## -description

Deletes a custom Jump List for a specified application.

## -parameters

### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process whose taskbar button representation displays the custom Jump List. In the beta release of Windows 7, this AppUserModelID must be explicitly provided because this method is intended to be called from an uninstaller, which runs in a separate process. Because it is in a separate process, the system cannot reliably deduce the AppUserModelID. This restriction is expected to be removed in later releases.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There are several instances where this method should be called, including:
            
                

<ul>
<li>When the application is uninstalled.</li>
<li>When the user clears history from within the application.</li>
<li>When the user disables destination tracking in the application's Settings or Options pages.</li>
</ul>
This method should not be called when an application is updating a custom destination list. It is used only to completely clear the list during an uninstall operation, or if the application provides an option for the user to turn off the list.

After the custom Jump List has been removed, a standard Jump List generated from system-generated data for recently used items is shown. If no such data has been collected or if the information has been cleared through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-removealldestinations">RemoveAllDestinations</a>, the Jump List might contain only its minimum, always present content: standard tasks to pin or unpin, launch a new instance of the application, or close windows.

## -see-also

<a href="/windows/desktop/shell/appids">Application User Model IDs (AppUserModelIDs)</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid">ICustomDestinationList::SetAppID</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>