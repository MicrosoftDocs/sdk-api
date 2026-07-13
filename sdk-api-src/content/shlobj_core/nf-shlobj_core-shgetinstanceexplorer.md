---
UID: NF:shlobj_core.SHGetInstanceExplorer
title: SHGetInstanceExplorer function (shlobj_core.h)
description: Retrieves an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.
helpviewer_keywords: ["SHGetInstanceExplorer","SHGetInstanceExplorer function [Windows Shell]","_win32_SHGetInstanceExplorer","shell.SHGetInstanceExplorer","shlobj_core/SHGetInstanceExplorer"]
old-location: shell\SHGetInstanceExplorer.htm
tech.root: shell
ms.assetid: ac6d8f7d-2eae-4b22-b493-b4ef740e3c95
ms.date: 12/05/2018
ms.keywords: SHGetInstanceExplorer, SHGetInstanceExplorer function [Windows Shell], _win32_SHGetInstanceExplorer, shell.SHGetInstanceExplorer, shlobj_core/SHGetInstanceExplorer
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetInstanceExplorer
 - shlobj_core/SHGetInstanceExplorer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell32-shellfolders-l1-2-1.dll
 - ext-ms-win-shell32-shellfolders-l1-2-0.dll
 - api-ms-win-shell-shellfolders-l1-1-1.dll
 - Shell32.dll
 - API-MS-Win-shell-shellfolders-l1-1-0.dll
 - KernelBase.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-0.dll
 - Ext-MS-Win-Shell32-Shellfolders-L1-1-1.dll
 - Windows.Storage.dll
api_name:
 - SHGetInstanceExplorer
---

# SHGetInstanceExplorer function


## -description

Retrieves an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. The host process is typically Windows Explorer or Windows Internet Explorer, but this function can also be used by other applications.

## -parameters

### -param ppunk [out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

When this function returns successfully, contains the address of the host process' <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer. This is a free-threaded interface used to prevent the host process from terminating. If the function call fails, this value is set to <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There are a number of components, such as Shell extension handlers, that are implemented as DLLs and run in a host process such as Windows Explorer (Explorer.exe) or Internet Explorer (Iexplore.exe). Typically, when the user closes the host process, the component is shut down immediately as well. Such an abrupt termination can create problems for some components. For example, if a component is using a background thread to download data or run user-interface functions, it might need additional time to safely shut itself down.

<b>SHGetInstanceExplorer</b> allows components that run in a host process to hold a reference on the host process. <b>SHGetInstanceExplorer</b> increments the host's reference count and returns a pointer to the host's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. By holding that reference, a component can prevent the host process from closing prematurely. After the component has completed its necessary processing, it should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">(*ppunk)->Release</a> to release the host's reference and allow the process to terminate.

<div class="alert"><b>Note</b>  If <b>SHGetInstanceExplorer</b> is successful, the component must release the host's reference when it is no longer needed. Otherwise, all resources associated with the process will remain in memory. The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointed to by *<i>ppunk</i> can only be used to release this reference. Components cannot use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">(*ppunk)->QueryInterface</a> to request other interface pointers.</div>
<div> </div>
<b>SHGetInstanceExplorer</b> succeeds only if it is called from from an application which had previously called <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer">SHSetInstanceExplorer</a> to set a process reference.