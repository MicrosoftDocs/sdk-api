---
UID: NF:mfapi.MFRegisterPlatformWithMMCSS
title: MFRegisterPlatformWithMMCSS function
author: windows-sdk-content
description: Registers the standard Microsoft Media Foundation platform work queues with the Multimedia Class Scheduler Service (MMCSS).
old-location: mf\mfregisterplatformwithmmcss.htm
tech.root: medfound
ms.assetid: 8F99849B-5363-4EEF-BCB8-C69A5309AF34
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MFRegisterPlatformWithMMCSS, MFRegisterPlatformWithMMCSS function [Media Foundation], mf.mfregisterplatformwithmmcss, mfapi/MFRegisterPlatformWithMMCSS, mfplat/MFRegisterPlatformWithMMCSS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
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
 - MFRegisterPlatformWithMMCSS
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFRegisterPlatformWithMMCSS function


## -description


Registers the standard Microsoft Media Foundation platform work queues with the Multimedia Class Scheduler Service (MMCSS).



## -parameters




### -param wszClass [in]

The name of the MMCSS task.




### -param pdwTaskId [in, out]

The MMCSS task identifier. On input, specify an existing  MCCSS task group ID, or use the value zero to create a new task group. On output, receives the actual task group ID.


### -param lPriority [in]

The base priority of the work-queue threads.




## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To unregister the platform work queues from the MMCSS class, call <a href="https://msdn.microsoft.com/B080E515-AD0E-492D-A9EF-8391DCEC3891">MFUnregisterPlatformFromMMCSS</a>.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>
 

 

