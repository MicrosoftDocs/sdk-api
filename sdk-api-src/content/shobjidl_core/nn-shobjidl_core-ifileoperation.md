---
UID: NN:shobjidl_core.IFileOperation
title: IFileOperation (shobjidl_core.h)
author: windows-sdk-content
description: Exposes methods to copy, move, rename, create, and delete Shell items as well as methods to provide progress and error dialogs. This interface replaces the SHFileOperation function.
old-location: shell\IFileOperation.htm
tech.root: shell
ms.assetid: 6596607e-0699-4eb6-b0d6-7cc2e5eb49c7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFileOperation, IFileOperation interface [Windows Shell], IFileOperation interface [Windows Shell],described, _shell_IFileOperation, shell.IFileOperation, shobjidl_core/IFileOperation
ms.topic: interface
f1_keywords: ["shobjidl_core/IFileOperation"]
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IFileOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFileOperation interface


## -description


Exposes methods to copy, move, rename, create, and delete Shell items as well as methods to provide progress and error dialogs. This interface replaces the <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileOperation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">Advise</a>
</td>
<td align="left" width="63%">
Enables a handler to provide status and error information for all operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitem">ApplyPropertiesToItem</a>
</td>
<td align="left" width="63%">
Declares a single item whose property values are to be set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitems">ApplyPropertiesToItems</a>
</td>
<td align="left" width="63%">
Declares a set of items for which to apply a common set of property values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">CopyItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be copied to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitems">CopyItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be copied to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">DeleteItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitems">DeleteItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-getanyoperationsaborted">GetAnyOperationsAborted</a>
</td>
<td align="left" width="63%">
Gets a value that states whether any file operations initiated by a call to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">IFileOperation::PerformOperations</a> were stopped before they were complete. The operations could be stopped either by user action or silently by the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitem">MoveItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be moved to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitems">MoveItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be moved to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-newitem">NewItem</a>
</td>
<td align="left" width="63%">
Declares a new item that is to be created in a specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">PerformOperations</a>
</td>
<td align="left" width="63%">
Executes all selected operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">RenameItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be given a new display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitems">RenameItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be given a new display name. All items are given the same name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setoperationflags">SetOperationFlags</a>
</td>
<td align="left" width="63%">
Sets parameters for the current operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setownerwindow">SetOwnerWindow</a>
</td>
<td align="left" width="63%">
Sets the parent or owner window for progress and dialog windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setprogressdialog">SetProgressDialog</a>
</td>
<td align="left" width="63%">
Specifies a dialog box used to display the progress of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setprogressmessage">SetProgressMessage</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setproperties">SetProperties</a>
</td>
<td align="left" width="63%">
Declares a set of properties and values to be set on an item or items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection previously established through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a>.

</td>
</tr>
</table> 


## -remarks



A Shell item can be any object in the namespace, including file system objects such as files and folders, but also virtual objects. In the <b>IFileOperation</b> method topics, the term "item" is used to refer generically to any namespace object.

<b>IFileOperation</b> offers many advantages over the older <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.

                

<ul>
<li>Use of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> to identify items rather than string paths. <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> required path and destination strings to terminate in two null characters rather than the standard single null character, which itself was used to delimit multiple paths in the string. Identifying an item through <b>IShellItem</b> is more robust and less prone to programming errors. It also allows you to access non-file system items such as virtual folders. Multiple items in one operation can be passed as an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray">IShellItemArray</a>, <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>, or a collection accessed through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a> rather than as a string.
                    </li>
<li>More accurate error reporting through HRESULT values in conjunction with an API such as <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>. Return codes from <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> could be misleading or inaccurate.</li>
<li>Extensibility. As a Component Object Model (COM) interface, <b>IFileOperation</b> can have its capabilities extended by a third-party to meet their specific needs, although this should be a very rare case. Windows provides a default implementation of <b>IFileOperation</b> that should meet the needs of most users.</li>
<li>Better progress feedback. Detailed operation progress, including notifications when specific operations begin and end on individual items as well as the overall progress, can be received during the operation. While <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> did provide progress UI, it was not as detailed.</li>
<li>More functionality. In addition to the copy, delete, move, and rename functionality provided by <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a>, <b>IFileOperation</b> allows you to apply property values and create new items.</li>
<li>More control over the operation. In addition to the operation flags recognized by <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a>, new flags are recognized in <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setoperationflags">IFileOperation::SetOperationFlags</a> that specify extended operation options.</li>
<li>Different operations can be performed in one call. For instance, you can move a set of files, copy others, rename a folder, and apply properties to yet another item all in one operation. <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> could only do one operation—copy, move, rename, or delete—at a time.</li>
</ul>
To accomplish a file operation using this interface, a sequence of calls must be made.

                

<ol>
<li>Optional. Set up the event sink for progress status and error notifications through <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">Advise</a> and <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-unadvise">Unadvise</a>.</li>
<li>Set the operation state using the following as needed:
                        <ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setoperationflags">SetOperationFlags</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setownerwindow">SetOwnerWindow</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setprogressdialog">SetProgressDialog</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setprogressmessage">SetProgressMessage</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-setproperties">SetProperties</a>
</li>
</ul>
</li>
<li>Specify which operations to perform on which items using the following as needed.

                        <ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitem">ApplyPropertiesToItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-applypropertiestoitems">ApplyPropertiesToItems</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">CopyItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitems">CopyItems</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">DeleteItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitems">DeleteItems</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitem">MoveItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitems">MoveItems</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-newitem">NewItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">RenameItem</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitems">RenameItems</a>
</li>
</ul>
</li>
<li>Execute the operations by calling <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-performoperations">PerformOperations</a>
</li>
</ol>
<b>IFileOperation</b> can only be applied in a single-threaded apartment (STA) situation. It cannot be used for a multithreaded apartment (MTA) situation. For MTA, you still must use <a href="https://docs.microsoft.com/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a>.

A full sample that demonstrates the extension of <b>IFileOperation</b> is included in the Windows Software Development Kit (SDK). In a default installation, it can be found at %ProgramFiles%\Microsoft SDKs\Windows\v6.0\Samples\WinUI\Shell\AppPlatform\FileOperations.



