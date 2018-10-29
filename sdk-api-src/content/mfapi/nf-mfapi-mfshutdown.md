---
UID: NF:mfapi.MFShutdown
title: MFShutdown function
author: windows-sdk-content
description: Shuts down the Microsoft Media Foundation platform.
old-location: mf\mfshutdown.htm
tech.root: medfound
ms.assetid: 10be2361-b5b4-4c10-92a1-527ca22c74e4
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: 10be2361-b5b4-4c10-92a1-527ca22c74e4, MFShutdown, MFShutdown function [Media Foundation], mf.mfshutdown, mfapi/MFShutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFShutdown function


## -description


Shuts down the Microsoft Media Foundation platform. Call this function once for every call to <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a>. Do not call this function from work queue threads.


## -parameters






## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e4db81d3-7a9e-47d7-8611-6dac8026259c">Initializing Media Foundation</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

