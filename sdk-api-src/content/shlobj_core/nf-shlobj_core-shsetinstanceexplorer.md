---
UID: NF:shlobj_core.SHSetInstanceExplorer
title: SHSetInstanceExplorer function
author: windows-driver-content
description: Provides an interface that allows hosted Shell extensions and other components to prevent their host process from closing prematurely.
old-location: shell\SHSetInstanceExplorer.htm
old-project: shell
ms.assetid: 86f29587-8347-4e88-87bc-83ef2b8a7728
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: SHSetInstanceExplorer, SHSetInstanceExplorer function [Windows Shell], _win32_SHSetInstanceExplorer, shell.SHSetInstanceExplorer, shlobj_core/SHSetInstanceExplorer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: AUTOCOMPLETELISTOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shell32.dll
-	ext-ms-win-shell-shell32-l1-2-1.dll
-	Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
-	SHSetInstanceExplorer
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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
 

 

