---
UID: NF:winddi.EngUnlockDriverObj
title: EngUnlockDriverObj function
author: windows-sdk-content
description: The EngUnlockDriverObj function causes GDI to unlock the driver object.
old-location: display\engunlockdriverobj.htm
old-project: display
ms.assetid: 027bf180-b226-4d88-803d-2839417f727f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: EngUnlockDriverObj, EngUnlockDriverObj function [Display Devices], display.engunlockdriverobj, gdifncs_3d830c51-4f44-40ef-933b-d04fed38523c.xml, winddi/EngUnlockDriverObj
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
 - EngUnlockDriverObj
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngUnlockDriverObj function


## -description


The <b>EngUnlockDriverObj</b> function causes GDI to unlock the driver object.


## -parameters




### -param hdo

Identifies the object to be unlocked.


## -returns



The return value is <b>TRUE</b> if the function is successful; otherwise, it is <b>FALSE</b>.




## -remarks



The specified driver object must have been previously locked by a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>. The object is not unlockable by another thread while it is locked down.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564967">EngLockDriverObj</a>
 

 

