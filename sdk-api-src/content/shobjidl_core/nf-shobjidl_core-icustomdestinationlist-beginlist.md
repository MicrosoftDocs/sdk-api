---
UID: NF:shobjidl_core.ICustomDestinationList.BeginList
title: ICustomDestinationList::BeginList (shobjidl_core.h)
description: Initiates a building session for a custom Jump List.
helpviewer_keywords: ["BeginList","BeginList method [Windows Shell]","BeginList method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","BeginList method","ICustomDestinationList.BeginList","ICustomDestinationList::BeginList","_shell_ICustomDestinationList_BeginList","shell.ICustomDestinationList_BeginList","shobjidl_core/ICustomDestinationList::BeginList"]
old-location: shell\ICustomDestinationList_BeginList.htm
tech.root: shell
ms.assetid: 431ae6b0-1421-46ec-a06a-38158acb0275
ms.date: 12/05/2018
ms.keywords: BeginList, BeginList method [Windows Shell], BeginList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],BeginList method, ICustomDestinationList.BeginList, ICustomDestinationList::BeginList, _shell_ICustomDestinationList_BeginList, shell.ICustomDestinationList_BeginList, shobjidl_core/ICustomDestinationList::BeginList
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
 - ICustomDestinationList::BeginList
 - shobjidl_core/ICustomDestinationList::BeginList
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
 - ICustomDestinationList.BeginList
---

# ICustomDestinationList::BeginList


## -description

Initiates a building session for a custom Jump List.

## -parameters

### -param pcMinSlots [out]

Type: <b>UINT*</b>

A pointer that, when this method returns, points to the current user setting for the <b>Number of recent items to display in Jump Lists</b> option in the <b>Taskbar and Start Menu Properties</b> window. The default value is 10. This is the maximum number of destinations that will be shown, and it is a total of all destinations, regardless     of category. More destinations can be added, but they will not be shown in the UI.



A Jump List will always show at least this many slots—destinations and, if there is room, tasks.

This number does not include separators and section headers as long as the total number of separators and headers does not exceed four. Separators and section headers beyond the first four might reduce the number of destinations displayed if space is constrained. This number does not affect the standard command entries for pinning or unpinning, closing the window, or launching a new instance. It also does not affect tasks or pinned items, the number of which that can be displayed is based on the space available to the Jump List.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of an interface to be retrieved in <i>ppv</i>, typically IID_IObjectArray, that will represent all items currently stored in the list of removed destinations for the application. This information is used to ensure that removed items are not part of the new Jump List.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically an <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a>, which represents a collection of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> objects that represent the removed items.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If an application has an explicit Application User Model ID (AppUserModelID), you must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid">ICustomDestinationList::SetAppID</a> before you call this method.

The <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a> interface retrieved in the <i>ppv</i> parameter represents the same list of removed destinations that is retrieved through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-getremoveddestinations">GetRemovedDestinations</a>. When a new Jump List is being generated, applications must first process any removed destinations. Tracking data for any item in the removed list must be cleared. If an application attempts to include an item through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a> that is present in this removed destinations list, the <b>AppendCategory</b> call fails. This ensures that applications respect the user's choice of removed items. After a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-commitlist">CommitList</a> is made with no failed call to <b>AppendCategory</b> due to an attempt to re-add a removed item having been made since <b>BeginList</b>, the removed destinations list is cleared. After that time, a previously removed item can return to the destinations list if the user continues to use the item.

<b>BeginList</b> must be called to initiate the list before any calls are made to populate it through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a>, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendknowncategory">AppendKnownCategory</a>, or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks">AddUserTasks</a>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>