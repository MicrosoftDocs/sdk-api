---
UID: NF:winddi.EngLoadModule
title: EngLoadModule function
author: windows-sdk-content
description: The EngLoadModule function loads the specified data module into system memory for reading.
old-location: display\engloadmodule.htm
old-project: display
ms.assetid: 0327d3f0-f9ee-4715-aa0e-ad1d0544a1ff
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: EngLoadModule, EngLoadModule function [Display Devices], display.engloadmodule, gdifncs_43b05b8f-ecc9-4097-81d3-39716dabaf2f.xml, winddi/EngLoadModule
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
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



<b>EngLoadModule</b> loads a data file into system memory with read-only permission. To access the loaded module, the driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a> with the handle returned by this function.

The file identified by <i>pwsz</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

To load a writable module, the driver should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>. Drivers that need to load an image as executable code should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564963">EngLoadImage</a> instead of this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564902">EngFreeModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564974">EngMapModule</a>
 

 

