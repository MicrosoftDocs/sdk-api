---
UID: NF:shobjidl_core.ICustomDestinationList.AddUserTasks
title: ICustomDestinationList::AddUserTasks (shobjidl_core.h)
description: Specifies items to include in the Tasks category of a custom Jump List.
helpviewer_keywords: ["AddUserTasks","AddUserTasks method [Windows Shell]","AddUserTasks method [Windows Shell]","ICustomDestinationList interface","ICustomDestinationList interface [Windows Shell]","AddUserTasks method","ICustomDestinationList.AddUserTasks","ICustomDestinationList::AddUserTasks","_shell_ICustomDestinationList_AddUserTasks","shell.ICustomDestinationList_AddUserTasks","shobjidl_core/ICustomDestinationList::AddUserTasks"]
old-location: shell\ICustomDestinationList_AddUserTasks.htm
tech.root: shell
ms.assetid: 7b254276-dc6f-4d20-8f44-fce8e01b237f
ms.date: 12/05/2018
ms.keywords: AddUserTasks, AddUserTasks method [Windows Shell], AddUserTasks method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],AddUserTasks method, ICustomDestinationList.AddUserTasks, ICustomDestinationList::AddUserTasks, _shell_ICustomDestinationList_AddUserTasks, shell.ICustomDestinationList_AddUserTasks, shobjidl_core/ICustomDestinationList::AddUserTasks
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
 - ICustomDestinationList::AddUserTasks
 - shobjidl_core/ICustomDestinationList::AddUserTasks
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
 - ICustomDestinationList.AddUserTasks
---

# ICustomDestinationList::AddUserTasks


## -description

Specifies items to include in the <b>Tasks</b> category of a custom Jump List.

## -parameters

### -param poa [in]

Type: <b><a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a>*</b>

A pointer to an <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a> that represents one or more <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> (or, more rarely, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>) objects that represent the tasks.

                    

<div class="alert"><b>Note</b>  Any <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> used here must declare an argument list through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments">SetArguments</a>. Adding an <b>IShellLink</b> object with no arguments to a custom category is not supported. A user cannot pin or unpin this type of item from a Jump List, nor can they be added or removed.</div>
<div> </div>

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.

## -remarks

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> before you call this method.

The <b>Tasks</b> category header is always shown in the list by default, unless the category is empty. This header text cannot be changed. It is displayed in the user's selected language.

The <b>Tasks</b> category, even though it always appears as the last category in a Jump List, takes priority over all other categories in the list. This list is filled, and then the remaining space is allocated to the other categories. Unlike other categories, items in the <b>Tasks</b> category cannot be removed or pinned by the user. Applications must balance the value to the user of the tasks in this category against the space needed for other categories.

Tasks should apply to the application as a whole; they are not meant to be specific to an individual window or document. For those more granular contextual tasks, an application can supply them through a <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons">thumbnail toolbar</a>.

<div class="alert"><b>Note</b>  It is strongly recommended that the task list be static. The task list should remain the same regardless of the state or status of the application—these tasks are available even when the application is not running. There is no programmatic prohibition against using <b>AddUserTasks</b> to vary the task list when it is updated, but you should consider that this could confuse the user who does not expect that portion of the Jump List to change. However, if an application does opt to change the state of a task, such as "Sign In" to "Sign Out", it is the responsibility of that application to ensure that the task list is correct and up to date. Also, if the application unexpectedly shuts down, the taskbar will use its last known good version of the task list without calling into the application to request one, leading to the possibility of out of date items.</div>
<div> </div>

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> instances provided through the <a href="/windows/desktop/api/objectarray/nn-objectarray-iobjectarray">IObjectArray</a> pointed to by <i>poa</i> must provide the following:

                

<ul>
<li>Either a pointer to an item identifier list (PIDL) (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setidlist">SetIDList</a>) or the target path (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setpath">SetPath</a> or <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setrelativepath">SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments">SetArguments</a>)</li>
<li>Icon location  (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-seticonlocation">SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="/windows/desktop/properties/props-system-title">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription">SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.

A task list can also include separators. These are created by including a blank <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> (this is the single exception to the argument list requirement), and setting its <a href="/windows/desktop/properties/props-system-appusermodel-isdestlistseparator">System.AppUserModel.IsDestListSeparator</a> property to <b>TRUE</b> through the <b>IShellLink</b> object's <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> interface. Any other values in the <b>IShellLink</b> will be ignored. Separators do not take up a full space in the list and are not counted in the number of items in the list. If two separators are provided with no items between them, one of the separators will not be shown. Separators at the beginning or end of the list are also ignored.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist">ICustomDestinationList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">ICustomDestinationList::AppendCategory</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendknowncategory">ICustomDestinationList::AppendKnownCategory</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>