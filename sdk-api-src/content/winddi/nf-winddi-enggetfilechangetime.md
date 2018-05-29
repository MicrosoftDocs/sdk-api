---
UID: NF:winddi.EngGetFileChangeTime
title: EngGetFileChangeTime function
author: windows-sdk-content
description: The EngGetFileChangeTime function retrieves a file's last write time.
old-location: display\enggetfilechangetime.htm
old-project: display
ms.assetid: fd3330e4-af51-4f4c-bc4f-1b08502009bd
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EngGetFileChangeTime, EngGetFileChangeTime function [Display Devices], display.enggetfilechangetime, gdifncs_627ace85-186b-4fe7-bd50-f8f0fb7da105.xml, winddi/EngGetFileChangeTime
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Win32k.sys
api_name:
-	EngGetFileChangeTime
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngGetFileChangeTime function


## -description


The <b>EngGetFileChangeTime</b> function retrieves a file's last write time.


## -parameters




### -param h [in]

Handle to the file whose change time is to be queried.


### -param pChangeTime [out]

Pointer to a LARGE_INTEGER in which the change time is returned.


## -returns



<b>EngGetFileChangeTime</b> returns <b>TRUE</b> if it succeeds in returning the timestamp; otherwise it returns <b>FALSE</b>.




## -remarks



The time returned is specified in system-time format. Absolute system time is the number of 100-nanosecond intervals since the start of the year 1601.



