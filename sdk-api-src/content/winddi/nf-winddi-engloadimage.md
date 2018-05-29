---
UID: NF:winddi.EngLoadImage
title: EngLoadImage macro
author: windows-sdk-content
description: The EngLoadImage function loads the specified executable image into kernel-mode memory.
old-location: display\engloadimage.htm
old-project: display
ms.assetid: 03b1835a-5c4e-4f38-93b1-e557a2975be7
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngLoadImage, EngLoadImage function [Display Devices], display.engloadimage, gdifncs_8fb20a2d-c7ae-4d15-af65-219b44289130.xml, winddi/EngLoadImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngLoadImage
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngLoadImage macro


## -description


The <b>EngLoadImage</b> function loads the specified executable image into kernel-mode memory.


## -parameters




### -param filename

TBD






#### - pwszDriver [in]

Pointer to a null-terminated string that names the file containing the executable image to be loaded.


## -remarks



A driver can use <b>EngLoadImage</b> to map an executable image into kernel-mode memory. For example, a printer driver can call <b>EngLoadImage</b> to load a minidriver.

<b>EngLoadImage</b> requires that the image file to be loaded have a <i>.dll</i> suffix. The driver must include this suffix in the <i>pwszDriver</i> string.

To execute a section of code within the loaded image, the driver should obtain the function address from <a href="https://msdn.microsoft.com/library/windows/hardware/ff564865">EngFindImageProcAddress</a>.

The file identified by <i>pwszDriver</i> must be located in the <i>%SystemRoot%\System32</i> directory or within a directory found in the directory hierarchy under <i>%SystemRoot%\System32</i>.

Drivers that need to load a module as data only should call <a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a> instead of this function.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564964">EngLoadModule</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff564965">EngLoadModuleForWrite</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff565041">EngUnloadImage</a>
 

 

