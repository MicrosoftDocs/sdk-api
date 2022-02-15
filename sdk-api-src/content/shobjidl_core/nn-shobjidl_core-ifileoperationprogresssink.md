---
UID: NN:shobjidl_core.IFileOperationProgressSink
title: IFileOperationProgressSink (shobjidl_core.h)
description: Exposes methods that provide a rich notification system used by callers of IFileOperation to monitor the details of the operations they are performing through that interface.
helpviewer_keywords: ["IFileOperationProgressSink","IFileOperationProgressSink interface [Windows Shell]","IFileOperationProgressSink interface [Windows Shell]","described","_shell_IFileOperationProgressSink","shell.IFileOperationProgressSink","shobjidl_core/IFileOperationProgressSink"]
old-location: shell\IFileOperationProgressSink.htm
tech.root: shell
ms.assetid: 24b20e05-d8be-4060-a966-7b32d9225403
ms.date: 12/05/2018
ms.keywords: IFileOperationProgressSink, IFileOperationProgressSink interface [Windows Shell], IFileOperationProgressSink interface [Windows Shell],described, _shell_IFileOperationProgressSink, shell.IFileOperationProgressSink, shobjidl_core/IFileOperationProgressSink
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFileOperationProgressSink
 - shobjidl_core/IFileOperationProgressSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileOperationProgressSink
---

# IFileOperationProgressSink interface


## -description

Exposes methods that provide a rich notification system used by callers of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> to monitor the details of the operations they are performing through that interface.

## -inheritance

The <b>IFileOperationProgressSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFileOperationProgressSink</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Applications must implement <b>IFileOperationProgressSink</b> themselves. Windows does not provide a default implementation.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
<b>IFileOperationProgressSink</b> are essentially handlers for particular events. They are used normally to display information about the specific action being processed at that time, such as the name of a file, source and destination, and the new name of the item at the destination. Post methods receive the HRESULT of each part of the operation so that the caller can determine specifically where the process fails if it does. <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> method parameter values are passed to the appropriate <b>IFileOperationProgressSink</b> methods so that they have access to the same information.

To attach an implementation of <b>IFileOperationProgressSink</b> to a call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>, you have two options:

                

<ul>
<li>To be advised of all operations performed by the call to <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>, use the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">IFileOperation::Advise</a> method.</li>
<li>To be notified only of progress for specific operations, pass <b>IFileOperationProgressSink</b> to one or more of these individual <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> methods:

<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-copyitem">CopyItem</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-deleteitem">DeleteItem</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-moveitem">MoveItem</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-newitem">NewItem</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-renameitem">RenameItem</a>
</li>
</ul>
</li>
</ul>
If you call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">Advise</a> there is no need to pass <b>IFileOperationProgressSink</b> to specific <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> methods as that results in redundant calls to the <b>IFileOperationProgressSink</b> methods and duplicate notifications.

If you choose to pass <b>IFileOperationProgressSink</b> only to select methods, the same instance of <b>IFileOperationProgressSink</b> can be used for them all.

<h3><a id="Example"></a><a id="example"></a><a id="EXAMPLE"></a>Example</h3>
The following example passes <b>IFileOperationProgressSink</b> to an instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a> by calling the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileoperation-advise">Advise</a> method.

                


```
IFileOperation *pfo;
CoCreateInstance(CLSID_FileOperation, NULL, CLSCTX_ALL, IID_IFileOperation, (void **)&m_pFO)
HRESULT hr = SHCreateFileOperation(hwnd, 0, IID_PPV_ARGS(&pfo));
if (SUCCEEDED(hr))
{
    // Advise to get notifications
    DWORD dwCookie;
    hr = pfo->Advise(SAFECAST(this, IFileOperationProgressSink*), &dwCookie);
}
```

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation">IFileOperation</a>
