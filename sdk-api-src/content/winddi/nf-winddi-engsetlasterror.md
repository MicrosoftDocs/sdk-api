---
UID: NF:winddi.EngSetLastError
title: EngSetLastError function
author: windows-sdk-content
description: The EngSetLastError function causes GDI to report an error code, which can be retrieved by an application.
old-location: display\engsetlasterror.htm
old-project: display
ms.assetid: 8887eed8-c60d-4217-92bf-f770be071c49
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngSetLastError, EngSetLastError function [Display Devices], display.engsetlasterror, gdifncs_696ff78e-c48b-4727-b2dd-d1b2e06ea90f.xml, winddi/EngSetLastError
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngSetLastError
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngSetLastError function


## -description


The <b>EngSetLastError</b> function causes GDI to report an error code, which can be retrieved by an application. 


## -parameters




### -param Arg1

TBD




#### - iError [in]

Specifies the 32-bit error code to set.


## -returns



None




## -remarks



<b>EngSetLastError</b> sets the last error code for the calling thread. This function allows a driver to communicate error conditions to an application. To facilitate this communication, a driver should use the Win32 application error codes defined in <i>winerror.h</i>.

Only the last error code to be set is retrievable; that is, consecutive calls to <b>EngSetLastError</b> will cause the last-error code field to be overwritten.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff564940">EngGetLastError</a>
 

 

