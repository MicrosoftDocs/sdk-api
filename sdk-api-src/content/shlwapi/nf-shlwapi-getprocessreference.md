---
UID: NF:shlwapi.GetProcessReference
title: GetProcessReference function (shlwapi.h)
description: Retrieves the process-specific object supplied by SetProcessReference, incrementing the reference count to keep the process alive.
helpviewer_keywords: ["GetProcessReference","GetProcessReference function [Windows Shell]","shell.GetProcessReference","shlwapi/GetProcessReference"]
old-location: shell\GetProcessReference.htm
tech.root: shell
ms.assetid: C46468A6-684D-494c-8261-87F16485B97B
ms.date: 12/05/2018
ms.keywords: GetProcessReference, GetProcessReference function [Windows Shell], shell.GetProcessReference, shlwapi/GetProcessReference
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
 - GetProcessReference
 - shlwapi/GetProcessReference
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
 - GetProcessReference
---

# GetProcessReference function


## -description

Retrieves the process-specific object supplied by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-setprocessreference">SetProcessReference</a>, incrementing the reference count to keep the process alive.

## -parameters

### -param punk [out]

The address of a pointer that, when this function returns successfully, points to the object supplied to the process by <a href="/windows/desktop/api/shlwapi/nf-shlwapi-setprocessreference">SetProcessReference</a>. Your application is responsible for freeing this resource when it is no longer needed.

A pointer to a free-threaded <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>. Components can use this interface (through <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>) to prevent the host process from terminating. This value can be <b>NULL</b>, in which case the process reference is no longer made available to components.

## -remarks

There are a number of components, such as Shell extension handlers, that are implemented as DLLs and run in a host process such as Windows Explorer (Explorer.exe) or Windows Internet Explorer (Iexplore.exe). Typically, when the user closes the host process, the component is shut down immediately as well. Such an abrupt termination can create problems for some components. For example, if a component is using a background thread to download data or run user-interface functions, it might need additional time to safely shut itself down.

<b>GetProcessReference</b> allows components that run in a host process to hold a reference on the host process. <b>GetProcessReference</b> increments the host's reference count and returns a pointer to the host's <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. By holding that reference, a component can prevent the host process from closing prematurely. After the component has completed its necessary processing, it should call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">(*punk)->Release</a> to release the host's reference and allow the process to terminate.

<div class="alert"><b>Note</b>  If <b>GetProcessReference</b> is successful, the component must release the host's reference when it is no longer needed. Otherwise, all resources associated with the process will remain in memory. The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointed to by *<i>punk</i> can only be used to release this reference. Components cannot use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">(*punk)->QueryInterface</a> to request other interface pointers.</div>
<div> </div>
<b>GetProcessReference</b> succeeds only if it is called from an application which had previously called <a href="/windows/desktop/api/shlwapi/nf-shlwapi-setprocessreference">SetProcessReference</a> to set a process reference.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetinstanceexplorer">SHGetInstanceExplorer</a>



<a href="/windows/desktop/api/shlwapi/nf-shlwapi-setprocessreference">SetProcessReference</a>



<a href="/windows/desktop/apiindex/windows-apisets">Windows API Sets</a>