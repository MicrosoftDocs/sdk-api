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

Each time a component calls <a href="https://msdn.microsoft.com/C46468A6-684D-494c-8261-87F16485B97B">GetProcessReference</a>, the system calls the <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> method before returning the interface pointer to the calling component. The component then calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> method when processing is complete. The process that calls <b>SetProcessReference</b> must not terminate while the reference count of the provided interface pointer is nonzero.

For further information on how components use the process references, see <a href="https://msdn.microsoft.com/C46468A6-684D-494c-8261-87F16485B97B">GetProcessReference</a>.




## -see-also




<a href="https://msdn.microsoft.com/C46468A6-684D-494c-8261-87F16485B97B">GetProcessReference</a>



<a href="https://msdn.microsoft.com/86f29587-8347-4e88-87bc-83ef2b8a7728">SHSetInstanceExplorer</a>



<a href="https://msdn.microsoft.com/0767BEA4-14C5-481A-8784-D3070C2E61DE">Windows API Sets</a>
 

 

