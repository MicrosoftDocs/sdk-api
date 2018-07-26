---
UID: NF:shlwapi.SetProcessReference
title: SetProcessReference function
author: windows-sdk-content
description: Provides a Component Object Model (COM) object that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.
old-location: shell\SetProcessReference.htm
old-project: shell
ms.assetid: 65C1BE1D-2C67-47a3-9958-38829BB8CCB0
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SetProcessReference, SetProcessReference function [Windows Shell], shell.SetProcessReference, shlwapi/SetProcessReference
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: URL_SCHEME
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
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Api-ms-win-shcore-thread-L1-1-0.dll
req.irql: 
req.product: Internet Explorer 6.01
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
 

 

