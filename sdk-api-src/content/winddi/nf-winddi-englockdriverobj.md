---
UID: NF:winddi.EngLockDriverObj
title: EngLockDriverObj function
author: windows-sdk-content
description: The EngLockDriverObj function creates an exclusive lock on this object for the calling thread.
old-location: display\englockdriverobj.htm
old-project: display
ms.assetid: 9ed3142d-2b20-4453-9057-80e6f8f92ff2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: EngLockDriverObj, EngLockDriverObj function [Display Devices], display.englockdriverobj, gdifncs_154bc925-ce22-45c9-8d24-724f186cd3b5.xml, winddi/EngLockDriverObj
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
api_name:
 - EngLockDriverObj
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngLockDriverObj function


## -description


The <b>EngLockDriverObj</b> function creates an exclusive lock on this object for the calling thread. 


## -parameters




### -param hdo

Handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a> structure to be locked by GDI.


## -returns



<b>EngLockDriverObj</b> returns a DRIVEROBJ structure if the function is successful. If the operation fails, it returns <b>NULL</b>. 




## -remarks



This function will fail if the handle is invalid, if the object is already locked by another thread, or if the handle is not owned by the calling process.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff556162">DRIVEROBJ</a>
 

 

