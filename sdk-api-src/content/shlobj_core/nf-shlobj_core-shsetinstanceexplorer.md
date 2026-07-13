---
UID: NF:shlobj_core.SHSetInstanceExplorer
title: SHSetInstanceExplorer function (shlobj_core.h)
description: Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.
helpviewer_keywords: ["SHSetInstanceExplorer","SHSetInstanceExplorer function [Windows Shell]","_win32_SHSetInstanceExplorer","shell.SHSetInstanceExplorer","shlobj_core/SHSetInstanceExplorer"]
old-location: shell\SHSetInstanceExplorer.htm
tech.root: shell
ms.assetid: 86f29587-8347-4e88-87bc-83ef2b8a7728
ms.date: 12/05/2018
ms.keywords: SHSetInstanceExplorer, SHSetInstanceExplorer function [Windows Shell], _win32_SHSetInstanceExplorer, shell.SHSetInstanceExplorer, shlobj_core/SHSetInstanceExplorer
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHSetInstanceExplorer
 - shlobj_core/SHSetInstanceExplorer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - SHSetInstanceExplorer
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHSetInstanceExplorer function


## -description

Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. The host process is typically Windows Explorer or Windows Internet Explorer, but this function can also be used by other applications.

## -parameters

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to a free-threaded <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. Components can use this interface (through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>) to prevent the host process from terminating. This value can be <b>NULL</b>, in which case the process reference is no longer made available to components.

## -remarks

Windows Explorer and Internet Explorer can use <b>SHSetInstanceExplorer</b> to allow components such as Shell extensions to extend the lifetime of the process. Other applications can also use <b>SHSetInstanceExplorer</b> to allow for the same capability. For instance, the browser message loop and the proxy desktop use <b>SHSetInstanceExplorer</b> to let other threads extend their lifetime.

Applications other than Windows Explorer and Internet Explorer that call this function might encounter compatibility problems because some components use <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a> to detect whether they are being hosted from within Windows Explorer or Internet Explorer.

The interface pointer passed to <b>SHSetInstanceExplorer</b> must reference a free-threaded object.

Each time a component calls <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>, the system calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method before returning the interface pointer to the calling component. The component then calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when processing is complete. The process that calls <b>SHSetInstanceExplorer</b> must not terminate while the reference count of the provided interface pointer is nonzero.

For further information on how components use the process references, see <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>
