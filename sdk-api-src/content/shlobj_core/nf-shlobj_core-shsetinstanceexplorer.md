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

# SHSetInstanceExplorer function


## -description


Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely. The host process is typically Windows Explorer or Windows Internet Explorer, but this function can also be used by other applications.


## -parameters




### -param punk [in, optional]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to a free-threaded <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>. Components can use this interface (through <a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>) to prevent the host process from terminating. This value can be <b>NULL</b>, in which case the process reference is no longer made available to components.


## -returns



This function does not return a value.




## -remarks



Windows Explorer and Internet Explorer can use <b>SHSetInstanceExplorer</b> to allow components such as Shell extensions to extend the lifetime of the process. Other applications can also use <b>SHSetInstanceExplorer</b> to allow for the same capability. For instance, the browser message loop and the proxy desktop use <b>SHSetInstanceExplorer</b> to let other threads extend their lifetime.

Applications other than Windows Explorer and Internet Explorer that call this function might encounter compatibility problems because some components use <a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a> to detect whether they are being hosted from within Windows Explorer or Internet Explorer.

The interface pointer passed to <b>SHSetInstanceExplorer</b> must reference a free-threaded object.

Each time a component calls <a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>, the system calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method before returning the interface pointer to the calling component. The component then calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when processing is complete. The process that calls <b>SHSetInstanceExplorer</b> must not terminate while the reference count of the provided interface pointer is nonzero.

For further information on how components use the process references, see <a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>.




## -see-also




<a href="https://msdn.microsoft.com/ac6d8f7d-2eae-4b22-b493-b4ef740e3c95">SHGetInstanceExplorer</a>
 

 

