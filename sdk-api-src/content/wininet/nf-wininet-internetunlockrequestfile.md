---
UID: NF:wininet.InternetUnlockRequestFile
title: InternetUnlockRequestFile function
author: windows-sdk-content
description: Unlocks a file that was locked using InternetLockRequestFile.
old-location: wininet\internetunlockrequestfile.htm
tech.root: wininet
ms.assetid: 356f7277-66ef-450f-ab5a-0303d0b1d807
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: InternetUnlockRequestFile, InternetUnlockRequestFile function [WinINet], _inet_internetunlockrequestfile_function, wininet.internetunlockrequestfile, wininet/InternetUnlockRequestFile
ms.topic: function
req.header: wininet.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wininet.lib
req.dll: Wininet.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wininet.dll
api_name:
 - InternetUnlockRequestFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InternetUnlockRequestFile function


## -description


Unlocks a file that was locked using 
<a href="https://msdn.microsoft.com/5924d117-1dcd-43d8-817e-02bda302bdd4">InternetLockRequestFile</a>.


## -parameters




### -param hLockRequestInfo [in]

Handle to a lock request that was returned by 
<a href="https://msdn.microsoft.com/5924d117-1dcd-43d8-817e-02bda302bdd4">InternetLockRequestFile</a>.


## -returns



Returns TRUE if successful, or FALSE otherwise. To get a specific error message, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c80768cf-c8c0-4bdf-9ea2-f82c92ade05a">Common Functions</a>



<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97">WinINet Functions</a>
 

 

