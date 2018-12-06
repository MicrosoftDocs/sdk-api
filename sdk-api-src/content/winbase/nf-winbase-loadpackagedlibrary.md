---
UID: NF:winbase.LoadPackagedLibrary
title: LoadPackagedLibrary function
author: windows-sdk-content
description: Loads the specified packaged module and its dependencies into the address space of the calling process.
old-location: base\loadpackagedlibrary.htm
tech.root: Dlls
ms.assetid: 4a103753-a2c9-487f-b797-01d5f5d489f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LoadPackagedLibrary, LoadPackagedLibrary function, base.loadpackagedlibrary, winbase/LoadPackagedLibrary
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-LibraryLoader-l2-1-0.dll
 - KernelBase.dll
api_name:
 - LoadPackagedLibrary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LoadPackagedLibrary function


## -description


Loads the specified packaged module and its dependencies into the address space of the calling process.


## -parameters




### -param lpwLibFileName [in]

The file name of the packaged module to load. The module can be a library module (a .dll file) or an executable module (an .exe file).  

If this parameter specifies a module name without a path and the file name extension is omitted, the function appends the default library extension .dll to the module name. To prevent the function from appending .dll to the module name, include a trailing point character (.) in the module name string. 

If this parameter specifies a path, the function searches that path for the module. The path cannot be an absolute path or a relative path that contains ".." in the path.   When specifying a path, be sure to use backslashes (\), not forward slashes (/). For more information about paths, see <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>. 

If the specified module is already loaded in the process, the function returns a handle to the loaded module. The module must have been originally loaded  from the package dependency graph of the process.

If loading the specified module causes the system to load other associated modules, the function first searches loaded modules, then it searches the package dependency graph of the process.  For more information, see Remarks.


### -param Reserved

This parameter is reserved. It must be 0.


## -returns



If the function succeeds, the return value is a handle to the loaded module.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The 
<b>LoadPackagedLibrary</b> function is a simplified version of <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>. Windows Runtime apps  can use <b>LoadPackagedLibrary</b> to load packaged modules. Desktop applications cannot use <b>LoadPackagedLibrary</b>; if a desktop application calls this function it fails with <b>APPMODEL_ERROR_NO_PACKAGE</b>.

<b>LoadPackagedLibrary</b> returns a handle to the specified module and increments its reference count. If the module is already loaded, the function returns a handle to the loaded module. The calling process can use the handle returned by <b>LoadPackagedLibrary</b> to identify the module in calls to the 
<a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function. Use the <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> function to free a loaded module and decrement its reference              count.  

If the function must search for the specified module or its dependencies, it searches only the package dependency graph of the process.  This is the application's package plus any dependencies specified as <code>&lt;PackageDependency&gt;</code> in the <code>&lt;Dependencies&gt;</code> section of the application's package manifest. Dependencies are searched in the order they appear in the manifest. The package dependency graph is specified in the <code>&lt;Dependencies&gt;</code> section of the application's package manifest. Dependencies are searched in the order they appear in the manifest. The search proceeds as follows: 

<ol>
<li>The function first searches modules that are already loaded. If the specified module was originally loaded from the package dependency graph of the process, the function returns a handle to the loaded module. If the specified module was not loaded from the package dependency graph of the process, the function returns <b>NULL</b>.</li>
<li>If the module is not already loaded, the function searches the package dependency graph of the process.</li>
<li>If the function cannot find the specified module or one of its dependencies, the function fails.</li>
</ol>
It is not safe to call 
<b>LoadPackagedLibrary</b> from 
<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a>. For more information, see the Remarks section in 
<b>DllMain</b>.



<div class="os_icon_block">
<ul class="os_icon_images">
<li><img alt="Applies to Windows Phone" src="../common/phone.png"/></li>
</ul>
<div class="os_icon_content_block">
<b>Note</b>  On Windows Phone, <b>LoadPackagedLibrary</b> must be called from <code>PhoneAppModelHost.dll</code>. Using <code>Kernel32.dll</code> is not supported.



</div>
</div>



## -see-also




<a href="https://msdn.microsoft.com/44228cf2-6306-466c-8f16-f513cd3ba8b5">Dynamic-Link Library Search Order</a>
 

 

