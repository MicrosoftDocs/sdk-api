---
UID: NF:winddi.EngLoadModule
title: EngLoadModule function
author: windows-sdk-content
description: The EngLoadModule function loads the specified data module into system memory for reading.
old-location: display\engloadmodule.htm
tech.root: display
ms.assetid: 0327d3f0-f9ee-4715-aa0e-ad1d0544a1ff
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EngLoadModule, EngLoadModule function [Display Devices], display.engloadmodule, gdifncs_43b05b8f-ecc9-4097-81d3-39716dabaf2f.xml, winddi/EngLoadModule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - EngLoadModule
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngLoadModule function


## -description


The <b>EngLoadModule</b> function loads the specified data module into system memory for reading.


## -parameters




### -param pwsz [in]

Pointer to a null-terminated string that contains the name of the data file to be loaded.


## -returns



If <b>EngLoadModule</b> succeeds, the return value is a handle to the module that was loaded. Otherwise, the return value is <b>NULL</b>.




## -remarks



<b>EngLoadModule</b> loads a data file into system memory with read-only permission. To access the loaded module, the driver should call <a href="https://msdn.microsoft.com/f8bd9b2c-11a3-454f-a4ce-cbda28115564">EngMapModule</a> with the handle returned by this function.

The file identified by <i>pwsz</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

To load a writable module, the driver should call <a href="https://msdn.microsoft.com/e5509142-624e-4c57-93b0-2579c6fb7089">EngLoadModuleForWrite</a>. Drivers that need to load an image as executable code should call <a href="https://msdn.microsoft.com/03b1835a-5c4e-4f38-93b1-e557a2975be7">EngLoadImage</a> instead of this function.




## -see-also




<a href="https://msdn.microsoft.com/f5520aec-5747-4970-ba2f-06b39e4f43f2">EngFreeModule</a>



<a href="https://msdn.microsoft.com/e5509142-624e-4c57-93b0-2579c6fb7089">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/f8bd9b2c-11a3-454f-a4ce-cbda28115564">EngMapModule</a>
 

 

