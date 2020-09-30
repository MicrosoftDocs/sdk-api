---
UID: NF:shlwapi.SetProcessReference
title: SetProcessReference function (shlwapi.h)
description: Provides a Component Object Model (COM) object that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.
helpviewer_keywords: ["SetProcessReference","SetProcessReference function [Windows Shell]","shell.SetProcessReference","shlwapi/SetProcessReference"]
old-location: shell\SetProcessReference.htm
tech.root: shell
ms.assetid: 65C1BE1D-2C67-47a3-9958-38829BB8CCB0
ms.date: 12/05/2018
ms.keywords: SetProcessReference, SetProcessReference function [Windows Shell], shell.SetProcessReference, shlwapi/SetProcessReference
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shlwapi.lib
req.dll: Api-ms-win-shcore-thread-L1-1-0.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetProcessReference
 - shlwapi/SetProcessReference
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-shcore-thread-L1-1-0.dll
 - ShCore.dll
api_name:
 - SetProcessReference
---

# SetProcessReference function


## -description

Provides a Component Object Model (COM) object that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. The host process is typically Windows Explorer or Windows Internet Explorer, but this function can also be used by other applications.

## -parameters

### -param punk [in, optional]

A pointer to the object for which you want to store a reference. This value can be <b>NULL</b>.

## -remarks

Windows Explorer and Internet Explorer can use <b>SetProcessReference</b> to allow components such as Shell extensions to extend the lifetime of the process. Other applications can also use <b>SetProcessReference</b> to allow for the same capability. For instance, the browser message loop and the proxy desktop use <b>SetProcessReference</b> to let other threads extend their lifetime.

Applications other than Windows Explorer and Internet Explorer that call this function might encounter compatibility problems because some components use <b>SetProcessReference</b> to detect whether they are being hosted from within Windows Explorer or Internet Explorer.

The interface pointer passed to <b>SetProcessReference</b> must reference a free-threaded object.

Each time a component calls <a href="/windows/desktop/api/shlwapi/nf-shlwapi-getprocessreference">GetProcessReference</a>, the system calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method before returning the interface pointer to the calling component. The component then calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method when processing is complete. The process that calls <b>SetProcessReference</b> must not terminate while the reference count of the provided interface pointer is nonzero.

For further information on how components use the process references, see <a href="/windows/desktop/api/shlwapi/nf-shlwapi-getprocessreference">GetProcessReference</a>.

## -see-also

<a href="/windows/desktop/api/shlwapi/nf-shlwapi-getprocessreference">GetProcessReference</a>



<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetinstanceexplorer">SHSetInstanceExplorer</a>



<a href="/windows/desktop/apiindex/windows-apisets">Windows API Sets</a>