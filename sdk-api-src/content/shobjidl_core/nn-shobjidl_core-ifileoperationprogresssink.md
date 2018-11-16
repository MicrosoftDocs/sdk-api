---
UID: NN:shobjidl_core.IFileOperationProgressSink
title: IFileOperationProgressSink
author: windows-sdk-content
description: Exposes methods that provide a rich notification system used by callers of IFileOperation to monitor the details of the operations they are performing through that interface.
old-location: shell\IFileOperationProgressSink.htm
tech.root: shell
ms.assetid: 24b20e05-d8be-4060-a966-7b32d9225403
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFileOperationProgressSink, IFileOperationProgressSink interface [Windows Shell], IFileOperationProgressSink interface [Windows Shell],described, _shell_IFileOperationProgressSink, shell.IFileOperationProgressSink, shobjidl_core/IFileOperationProgressSink
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperationProgressSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileOperationProgressSink interface


## -description


Exposes methods that provide a rich notification system used by callers of <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> to monitor the details of the operations they are performing through that interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFileOperationProgressSink</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFileOperationProgressSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFileOperationProgressSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d2d05c3-525d-4113-bb08-63395facf191">FinishOperations</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the last operation performed by the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8eaeb799-4e5e-4605-95b4-e574b87432c1">PauseTimer</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e5568a8-e689-48ca-82a1-36292d91a65b">PostCopyItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the copy process for each item is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bd69585-3801-4029-9f60-ab1e6fe5108c">PostDeleteItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the delete process for each item is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd353e15-4b1c-4d02-aa3f-c8d744a1722f">PostMoveItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the move process for each item is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/250ca9b8-951d-4ce8-bfb7-d512f4a59a39">PostNewItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the new item is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bb55ecf-a975-4e7f-9e41-30e778d4cbac">PostRenameItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions after the rename process for each item is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee436179-197d-49f6-986c-62a1ea930af5">PreCopyItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before the copy process for each item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf54f2da-4861-4546-9b1e-35b5983e836c">PreDeleteItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before the delete process for each item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd92c9fa-fdea-4149-9727-90eafdf7c6bc">PreMoveItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before the move process for each item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ea6223e1-a574-4e4b-a264-384f33579c6d">PreNewItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before the process to create a new item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/444fe15b-cbed-46d8-ae25-ab6a569d18e0">PreRenameItem</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before the rename process for each item begins.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b753b53d-4a54-4bb2-af94-dd296f86b37a">ResetTimer</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98886370-fce1-46f5-989d-e0625b196c49">ResumeTimer</a>
</td>
<td align="left" width="63%">
Not currently supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b9e4423-ead7-44be-b960-5ee83025f42a">StartOperations</a>
</td>
<td align="left" width="63%">
Performs caller-implemented actions before any specific file operations are performed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c61d4440-bcd3-46a7-8aeb-e5d80d0d53eb">UpdateProgress</a>
</td>
<td align="left" width="63%">
Provides an estimate of the total amount of work currently done in relation to the total amount of work.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications must implement <b>IFileOperationProgressSink</b> themselves. Windows does not provide a default implementation.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
<b>IFileOperationProgressSink</b> are essentially handlers for particular events. They are used normally to display information about the specific action being processed at that time, such as the name of a file, source and destination, and the new name of the item at the destination. Post methods receive the HRESULT of each part of the operation so that the caller can determine specifically where the process fails if it does. <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> method parameter values are passed to the appropriate <b>IFileOperationProgressSink</b> methods so that they have access to the same information.

To attach an implementation of <b>IFileOperationProgressSink</b> to a call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>, you have two options:

                

<ul>
<li>To be advised of all operations performed by the call to <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>, use the <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">IFileOperation::Advise</a> method.</li>
<li>To be notified only of progress for specific operations, pass <b>IFileOperationProgressSink</b> to one or more of these individual <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> methods:

                        <ul>
<li>
<a href="https://msdn.microsoft.com/36d623b7-67c3-48b7-be9b-9264b5b8d919">CopyItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/177ce480-0309-4ec8-a6f2-0be9196bd2c8">DeleteItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b1e66c9-5264-42cb-9554-d1ea92625c6f">MoveItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/810a1275-cae2-4487-b517-22aa8e4374a9">NewItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/2f72b729-3535-4ab7-9579-21b1ba97c67f">RenameItem</a>
</li>
</ul>
</li>
</ul>
If you call <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">Advise</a> there is no need to pass <b>IFileOperationProgressSink</b> to specific <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> methods as that results in redundant calls to the <b>IFileOperationProgressSink</b> methods and duplicate notifications.

If you choose to pass <b>IFileOperationProgressSink</b> only to select methods, the same instance of <b>IFileOperationProgressSink</b> can be used for them all.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following example passes <b>IFileOperationProgressSink</b> to an instance of <a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a> by calling the <a href="https://msdn.microsoft.com/458c24b0-9288-4ed7-9a4b-7534f26dd32e">Advise</a> method.

                

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IFileOperation *pfo;
CoCreateInstance(CLSID_FileOperation, NULL, CLSCTX_ALL, IID_IFileOperation, (void **)&amp;m_pFO)
HRESULT hr = SHCreateFileOperation(hwnd, 0, IID_PPV_ARGS(&amp;pfo));
if (SUCCEEDED(hr))
{
    // Advise to get notifications
    DWORD dwCookie;
    hr = pfo-&gt;Advise(SAFECAST(this, IFileOperationProgressSink*), &amp;dwCookie);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/6596607e-0699-4eb6-b0d6-7cc2e5eb49c7">IFileOperation</a>
 

 

