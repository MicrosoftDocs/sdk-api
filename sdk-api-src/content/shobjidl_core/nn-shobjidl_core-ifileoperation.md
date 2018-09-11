---
UID: NN:shobjidl_core.IFileOperation
title: IFileOperation
author: windows-sdk-content
description: Exposes methods to copy, move, rename, create, and delete Shell items as well as methods to provide progress and error dialogs. This interface replaces the SHFileOperation function.
old-location: shell\IFileOperation.htm
tech.root: shell
ms.assetid: 6596607e-0699-4eb6-b0d6-7cc2e5eb49c7
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IFileOperation, IFileOperation interface [Windows Shell], IFileOperation interface [Windows Shell],described, _shell_IFileOperation, shell.IFileOperation, shobjidl_core/IFileOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# IFileOperation interface


## -description


Exposes methods to copy, move, rename, create, and delete Shell items as well as methods to provide progress and error dialogs. This interface replaces the <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileOperation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileOperation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">Advise</a>
</td>
<td align="left" width="63%">
Enables a handler to provide status and error information for all operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">ApplyPropertiesToItem</a>
</td>
<td align="left" width="63%">
Declares a single item whose property values are to be set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d24aa63e-99ef-470c-9723-e561ee0a56bc">ApplyPropertiesToItems</a>
</td>
<td align="left" width="63%">
Declares a set of items for which to apply a common set of property values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/36d623b7-67c3-48b7-be9b-9264b5b8d919">CopyItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be copied to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9899cac2-bc10-422c-ab7f-2b8c1b893fc9">CopyItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be copied to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/177ce480-0309-4ec8-a6f2-0be9196bd2c8">DeleteItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/708072c4-c0c7-4d7d-a54f-234c57ff08e6">DeleteItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be deleted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/988f78a8-3a50-44d8-9214-7cf71be72d38">GetAnyOperationsAborted</a>
</td>
<td align="left" width="63%">
Gets a value that states whether any file operations initiated by a call to <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> were stopped before they were complete. The operations could be stopped either by user action or silently by the system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">MoveItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be moved to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b3c3fc9-5e08-44be-b0ba-a67702e2deb6">MoveItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be moved to a specified destination.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/810a1275-cae2-4487-b517-22aa8e4374a9">NewItem</a>
</td>
<td align="left" width="63%">
Declares a new item that is to be created in a specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">PerformOperations</a>
</td>
<td align="left" width="63%">
Executes all selected operations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">RenameItem</a>
</td>
<td align="left" width="63%">
Declares a single item that is to be given a new display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/325c09c6-ae32-4f5d-8b21-174dafc94aea">RenameItems</a>
</td>
<td align="left" width="63%">
Declares a set of items that are to be given a new display name. All items are given the same name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c2b9be8-d9b7-4ed4-a6da-e8166ddc35b3">SetOperationFlags</a>
</td>
<td align="left" width="63%">
Sets parameters for the current operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad3276a5-409d-4a49-ac95-2c2a3eb3b864">SetOwnerWindow</a>
</td>
<td align="left" width="63%">
Sets the parent or owner window for progress and dialog windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34cc6b88-9791-4778-a8d9-cf1b80aa42a8">SetProgressDialog</a>
</td>
<td align="left" width="63%">
Specifies a dialog box used to display the progress of the operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd8b4b00-3f41-41c4-aee0-89239ab70075">SetProgressMessage</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b54efc12-42e9-4a90-a4d9-0e75bcdba0d6">SetProperties</a>
</td>
<td align="left" width="63%">
Declares a set of properties and values to be set on an item or items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/684b3e94-50b9-465e-b4c3-b244fc7209f5">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates an advisory connection previously established through <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a>.

</td>
</tr>
</table> 


## -remarks



A Shell item can be any object in the namespace, including file system objects such as files and folders, but also virtual objects. In the <b>IFileOperation</b> method topics, the term "item" is used to refer generically to any namespace object.

<b>IFileOperation</b> offers many advantages over the older <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.

                

<ul>
<li>Use of <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> to identify items rather than string paths. <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> required path and destination strings to terminate in two null characters rather than the standard single null character, which itself was used to delimit multiple paths in the string. Identifying an item through <b>IShellItem</b> is more robust and less prone to programming errors. It also allows you to access non-file system items such as virtual folders. Multiple items in one operation can be passed as an <a href="https://msdn.microsoft.com/348213d1-c03f-4c38-9d13-3b1009d94e07">IShellItemArray</a>, <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>, or a collection accessed through <a href="https://msdn.microsoft.com/07aed597-359f-4f4b-9edf-168c15bdc58e">IEnumShellItems</a> rather than as a string.
                    </li>
<li>More accurate error reporting through HRESULT values in conjunction with an API such as <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a>. Return codes from <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> could be misleading or inaccurate.</li>
<li>Extensibility. As a Component Object Model (COM) interface, <b>IFileOperation</b> can have its capabilities extended by a third-party to meet their specific needs, although this should be a very rare case. Windows provides a default implementation of <b>IFileOperation</b> that should meet the needs of most users.</li>
<li>Better progress feedback. Detailed operation progress, including notifications when specific operations begin and end on individual items as well as the overall progress, can be received during the operation. While <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> did provide progress UI, it was not as detailed.</li>
<li>More functionality. In addition to the copy, delete, move, and rename functionality provided by <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a>, <b>IFileOperation</b> allows you to apply property values and create new items.</li>
<li>More control over the operation. In addition to the operation flags recognized by <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a>, new flags are recognized in <a href="https://msdn.microsoft.com/1c2b9be8-d9b7-4ed4-a6da-e8166ddc35b3">IFileOperation::SetOperationFlags</a> that specify extended operation options.</li>
<li>Different operations can be performed in one call. For instance, you can move a set of files, copy others, rename a folder, and apply properties to yet another item all in one operation. <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> could only do one operation—copy, move, rename, or delete—at a time.</li>
</ul>
To accomplish a file operation using this interface, a sequence of calls must be made.

                

<ol>
<li>Optional. Set up the event sink for progress status and error notifications through <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">Advise</a> and <a href="https://msdn.microsoft.com/684b3e94-50b9-465e-b4c3-b244fc7209f5">Unadvise</a>.</li>
<li>Set the operation state using the following as needed:
                        <ul>
<li>
<a href="https://msdn.microsoft.com/1c2b9be8-d9b7-4ed4-a6da-e8166ddc35b3">SetOperationFlags</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ad3276a5-409d-4a49-ac95-2c2a3eb3b864">SetOwnerWindow</a>
</li>
<li>
<a href="https://msdn.microsoft.com/34cc6b88-9791-4778-a8d9-cf1b80aa42a8">SetProgressDialog</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fd8b4b00-3f41-41c4-aee0-89239ab70075">SetProgressMessage</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b54efc12-42e9-4a90-a4d9-0e75bcdba0d6">SetProperties</a>
</li>
</ul>
</li>
<li>Specify which operations to perform on which items using the following as needed.

                        <ul>
<li>
<a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">ApplyPropertiesToItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d24aa63e-99ef-470c-9723-e561ee0a56bc">ApplyPropertiesToItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/36d623b7-67c3-48b7-be9b-9264b5b8d919">CopyItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9899cac2-bc10-422c-ab7f-2b8c1b893fc9">CopyItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/177ce480-0309-4ec8-a6f2-0be9196bd2c8">DeleteItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/708072c4-c0c7-4d7d-a54f-234c57ff08e6">DeleteItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">MoveItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b3c3fc9-5e08-44be-b0ba-a67702e2deb6">MoveItems</a>
</li>
<li>
<a href="https://msdn.microsoft.com/810a1275-cae2-4487-b517-22aa8e4374a9">NewItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">RenameItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/325c09c6-ae32-4f5d-8b21-174dafc94aea">RenameItems</a>
</li>
</ul>
</li>
<li>Execute the operations by calling <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">PerformOperations</a>
</li>
</ol>
<b>IFileOperation</b> can only be applied in a single-threaded apartment (STA) situation. It cannot be used for a multithreaded apartment (MTA) situation. For MTA, you still must use <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a>.

A full sample that demonstrates the extension of <b>IFileOperation</b> is included in the Windows Software Development Kit (SDK). In a default installation, it can be found at %ProgramFiles%\Microsoft SDKs\Windows\v6.0\Samples\WinUI\Shell\AppPlatform\FileOperations.



