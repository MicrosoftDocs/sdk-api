---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

