---
UID: NF:shlwapi.GetProcessReference
title: GetProcessReference function
author: windows-sdk-content
description: Retrieves the process-specific object supplied by SetProcessReference, incrementing the reference count to keep the process alive.
old-location: shell\GetProcessReference.htm
tech.root: shell
ms.assetid: C46468A6-684D-494c-8261-87F16485B97B
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetProcessReference, GetProcessReference function [Windows Shell], shell.GetProcessReference, shlwapi/GetProcessReference
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetProcessReference function


## -description


Retrieves the process-specific object supplied by <a href="https://msdn.microsoft.com/65C1BE1D-2C67-47a3-9958-38829BB8CCB0">SetProcessReference</a>, incrementing the reference count to keep the process alive.


## -parameters




### -param punk [out]

The address of a pointer that, when this function returns successfully, points to the object supplied to the process by <a href="https://msdn.microsoft.com/65C1BE1D-2C67-47a3-9958-38829BB8CCB0">SetProcessReference</a>. Your application is responsible for freeing this resource when it is no longer needed.

A pointer to a free-threaded <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Components can use this interface (through <a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>) to prevent the host process from terminating. This value can be <b>NULL</b>, in which case the process reference is no longer made available to components.


## -remarks



There are a number of components, such as Shell extension handlers, that are implemented as DLLs and run in a host process such as Windows Explorer (Explorer.exe) or Windows Internet Explorer (Iexplore.exe). Typically, when the user closes the host process, the component is shut down immediately as well. Such an abrupt termination can create problems for some components. For example, if a component is using a background thread to download data or run user-interface functions, it might need additional time to safely shut itself down.

<b>GetProcessReference</b> allows components that run in a host process to hold a reference on the host process. <b>GetProcessReference</b> increments the host's reference count and returns a pointer to the host's <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. By holding that reference, a component can prevent the host process from closing prematurely. After the component has completed its necessary processing, it should call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">(*punk)->Release</a> to release the host's reference and allow the process to terminate.

<div class="alert"><b>Note</b>  If <b>GetProcessReference</b> is successful, the component must release the host's reference when it is no longer needed. Otherwise, all resources associated with the process will remain in memory. The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointed to by *<i>punk</i> can only be used to release this reference. Components cannot use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">(*punk)->QueryInterface</a> to request other interface pointers.</div>
<div> </div>
<b>GetProcessReference</b> succeeds only if it is called from from an application which had previously called <a href="https://msdn.microsoft.com/65C1BE1D-2C67-47a3-9958-38829BB8CCB0">SetProcessReference</a> to set a process reference.




## -see-also




<a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>



<a href="https://msdn.microsoft.com/65C1BE1D-2C67-47a3-9958-38829BB8CCB0">SetProcessReference</a>



<a href="https://msdn.microsoft.com/0767BEA4-14C5-481A-8784-D3070C2E61DE">Windows API Sets</a>
 

 

