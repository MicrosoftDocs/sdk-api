---
UID: NF:shobjidl_core.ICustomDestinationList.AddUserTasks
title: ICustomDestinationList::AddUserTasks
author: windows-sdk-content
description: Specifies items to include in the Tasks category of a custom Jump List.
old-location: shell\ICustomDestinationList_AddUserTasks.htm
old-project: shell
ms.assetid: 7b254276-dc6f-4d20-8f44-fce8e01b237f
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: AddUserTasks, AddUserTasks method [Windows Shell], AddUserTasks method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],AddUserTasks method, ICustomDestinationList.AddUserTasks, ICustomDestinationList::AddUserTasks, _shell_ICustomDestinationList_AddUserTasks, shell.ICustomDestinationList_AddUserTasks, shobjidl_core/ICustomDestinationList::AddUserTasks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.AddUserTasks
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
req.product: Outlook Express 6.0
---

# ICustomDestinationList::AddUserTasks


## -description


Specifies items to include in the <b>Tasks</b> category of a custom Jump List.


## -parameters




### -param poa [in]

Type: <b><a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> that represents one or more <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> (or, more rarely, <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a>) objects that represent the tasks.

                    

<div class="alert"><b>Note</b>  Any <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> used here must declare an argument list through <a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">SetArguments</a>. Adding an <b>IShellLink</b> object with no arguments to a custom category is not supported. A user cannot pin or unpin this type of item from a Jump List, nor can they be added or removed.</div>
<div> </div>

## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise.




## -remarks



You must call <a href="https://msdn.microsoft.com/431ae6b0-1421-46ec-a06a-38158acb0275">ICustomDestinationList::BeginList</a> before you call this method.

The <b>Tasks</b> category header is always shown in the list by default, unless the category is empty. This header text cannot be changed. It is displayed in the user's selected language.

The <b>Tasks</b> category, even though it always appears as the last category in a Jump List, takes priority over all other categories in the list. This list is filled, and then the remaining space is allocated to the other categories. Unlike other categories, items in the <b>Tasks</b> category cannot be removed or pinned by the user. Applications must balance the value to the user of the tasks in this category against the space needed for other categories.

Tasks should apply to the application as a whole; they are not meant to be specific to an individual window or document. For those more granular contextual tasks, an application can supply them through a <a href="https://msdn.microsoft.com/5d573879-aa90-41d9-a9b7-b813dafa78ae">thumbnail toolbar</a>.

<div class="alert"><b>Note</b>  It is strongly recommended that the task list be static. The task list should remain the same regardless of the state or status of the application—these tasks are available even when the application is not running. There is no programmatic prohibition against using <b>AddUserTasks</b> to vary the task list when it is updated, but you should consider that this could confuse the user who does not expect that portion of the Jump List to change. However, if an application does opt to change the state of a task, such as "Sign In" to "Sign Out", it is the responsibility of that application to ensure that the task list is correct and up to date. Also, if the application unexpectedly shuts down, the taskbar will use its last known good version of the task list without calling into the application to request one, leading to the possibility of out of date items.</div>
<div> </div>

<a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> instances provided through the <a href="https://msdn.microsoft.com/ab0bb213-dc9c-4853-98d7-668e7ca76583">IObjectArray</a> pointed to by <i>poa</i> must provide the following:

                

<ul>
<li>Either a pointer to an item identifier list (PIDL) (<a href="https://msdn.microsoft.com/4c0571a5-1615-4c3f-b9a6-0667df07165b">SetIDList</a>) or the target path (<a href="https://msdn.microsoft.com/032610ba-d6ff-4200-8fd3-455460587dec">SetPath</a> or <a href="https://msdn.microsoft.com/f9cbd1db-253b-4ce8-a8ea-cfc48759c9d3">SetRelativePath</a>)</li>
<li>Command-line arguments (<a href="https://msdn.microsoft.com/5ad5fabd-be12-40bc-a6b3-498bcde7223a">SetArguments</a>)</li>
<li>Icon location  (<a href="https://msdn.microsoft.com/1ba267f2-ae05-4a6d-be3c-382a89e17d92">SetIconLocation</a>)</li>
</ul>
The display name must be set through the item's <a href="https://msdn.microsoft.com/8fb948d6-2677-4e5d-b283-8757c3df574d">System.Title (PKEY_Title)</a> property. The property can directly hold the display name or it can be an indirect string representation, such as "@shell32.dll,-1324", to use a stored string. An indirect string enables the item name to be displayed in the user's selected language.

Optionally, the description field (<a href="https://msdn.microsoft.com/4bec482e-04e6-4cde-ab8e-23c5a1463bdf">SetDescription</a>) can be set to provide a custom tooltip for the item in the Jump List.

A task list can also include separators. These are created by including a blank <a href="https://msdn.microsoft.com/67982d28-27ce-4482-b588-10fec8143750">IShellLink</a> (this is the single exception to the argument list requirement), and setting its <a href="https://msdn.microsoft.com/6cee1c20-865c-4d53-98c5-5402855a0004">System.AppUserModel.IsDestListSeparator</a> property to <b>TRUE</b> through the <b>IShellLink</b> object's <a href="https://msdn.microsoft.com/e995aaa1-d4c9-475f-b1fa-b9123cd5b653">IPropertyStore</a> interface. Any other values in the <b>IShellLink</b> will be ignored. Separators do not take up a full space in the list and are not counted in the number of items in the list. If two separators are provided with no items between them, one of the separators will not be shown. Separators at the beginning or end of the list are also ignored.




## -see-also




<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/091a2b28-b4cf-46a9-845a-46b5aa86522d">ICustomDestinationList::AppendCategory</a>



<a href="https://msdn.microsoft.com/ce73fff3-8d1a-4912-98ce-7149460ffa49">ICustomDestinationList::AppendKnownCategory</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

