---
UID: NN:shobjidl_core.ICustomDestinationList
title: ICustomDestinationList (shobjidl_core.h)
description: Exposes methods that allow an application to provide a custom Jump List, including destinations and tasks, for display in the taskbar.helpviewer_keywords: ["ICustomDestinationList","ICustomDestinationList interface [Windows Shell]","ICustomDestinationList interface [Windows Shell]","described","_shell_ICustomDestinationList","shell.ICustomDestinationList","shobjidl_core/ICustomDestinationList"]
old-location: shell\ICustomDestinationList.htm
tech.root: shell
ms.assetid: 65a3dab8-3136-416d-bd8a-ca813bfe0533
ms.date: 12/05/2018
ms.keywords: ICustomDestinationList, ICustomDestinationList interface [Windows Shell], ICustomDestinationList interface [Windows Shell],described, _shell_ICustomDestinationList, shell.ICustomDestinationList, shobjidl_core/ICustomDestinationList
f1_keywords:
- shobjidl_core/ICustomDestinationList
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shell32.dll
api_name:
- ICustomDestinationList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICustomDestinationList interface


## -description


Exposes methods that allow an application to provide a custom Jump List, including destinations and tasks, for display in the taskbar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICustomDestinationList</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICustomDestinationList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICustomDestinationList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-abortlist">AbortList</a>
</td>
<td align="left" width="63%">
Discontinues a Jump List building session initiated by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> without committing any changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks">AddUserTasks</a>
</td>
<td align="left" width="63%">
Specifies items to include in the <b>Tasks</b> category of a custom Jump List.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a>
</td>
<td align="left" width="63%">
Defines a custom category and the destinations that it contains, for inclusion in a custom Jump List.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendknowncategory">AppendKnownCategory</a>
</td>
<td align="left" width="63%">
Specifies that the <b>Frequent</b> or <b>Recent</b> category should be included in a custom Jump List.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">BeginList</a>
</td>
<td align="left" width="63%">
Initiates a building session for a custom Jump List.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-commitlist">CommitList</a>
</td>
<td align="left" width="63%">
Declares that the Jump List initiated by a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">ICustomDestinationList::BeginList</a> is complete and ready for display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-deletelist">DeleteList</a>
</td>
<td align="left" width="63%">
Deletes a custom Jump List for a specified application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-getremoveddestinations">GetRemovedDestinations</a>
</td>
<td align="left" width="63%">
Retrieves the current list of destinations that have been removed by the user from the existing Jump List that this custom Jump List is meant to replace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid">SetAppID</a>
</td>
<td align="left" width="63%">
Specifies a unique AppUserModelID for the application whose taskbar button will hold the custom Jump List built through the methods of this interface. This method is optional.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_DestinationList. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Jump Lists contain both destination and task lists.
            
                

<ul>
<li><i>Destinations</i> are items that appear in the <b>Recent</b>, <b>Frequent</b>, or custom categories, based on an individual's usage. Destinations can be files, folders, websites, or other content-based items, but are not necessarily file-backed. Destinations can be thought of as things or nouns. Destinations can be pinned or removed from the Jump List by the user. They are generally represented by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> objects but they can also be <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> objects.</li>
<li><i>Tasks</i> are common actions performed in an application that apply to all users of that application regardless of an individual's usage patterns. Tasks can be thought of as actions or verbs. Tasks cannot be pinned or removed. They are represented by <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a> objects.</li>
</ul>


The taskbar provides each taskbar button with a Jump List. By default, a Jump List contains a <b>Recent</b> category, which is populated automatically for file-based applications through <a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs">SHAddToRecentDocs</a> or the common file dialog. To replace the <b>Recent</b> category with the <b>Frequent</b> category or define, add, and populate its own custom categories, an application must call the methods of this interface. The application can also supply its own tasks based on the application's architecture and intended use.

<div class="alert"><b>Note</b>  An application must be a registered handler for a file type for an item of that type to appear in its Jump List. It does not, however, need to be the default handler for that file type.</div>
<div> </div>
A custom Jump List is intended to present content that the application has deemed significant based on either previous usage of the application or through an action that has indicated that an item is of importance to the user, such as the user adding an item to a Favorites list.

The application must call this object to provide a custom Jump List to the taskbar UI. The system never queries the application for the information.

When an application provides a custom Jump List, it takes on certain responsibilities around that list. Custom categories must be populated in a manner consistent with the intended use of a Jump List. Items in the list must be checked for validity or fail gracefully if they have been deleted. If the user removes an item from the list, that removal must be honored.

A custom Jump List is never truly updated in the sense of changing elements in an existing list. Rather, the old list is replaced with a new list.

The basic sequence of <b>ICustomDestinationList</b> method calls to build and display a custom Jump List is as follows:

                

<ol>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid">SetAppID</a> (required only if an application provides its own AppUserModelID)</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-beginlist">BeginList</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory">AppendCategory</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendknowncategory">AppendKnownCategory</a>, <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-addusertasks">AddUserTasks</a>, or any combination of those three methods.</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-commitlist">CommitList</a>
</li>
</ol>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
 

 

