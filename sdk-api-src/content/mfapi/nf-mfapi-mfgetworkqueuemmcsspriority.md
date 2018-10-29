---
UID: NF:mfapi.MFGetWorkQueueMMCSSPriority
title: MFGetWorkQueueMMCSSPriority function
author: windows-sdk-content
description: Gets the relative thread priority of a work queue.
old-location: mf\mfgetworkqueuemmcsspriority.htm
tech.root: medfound
ms.assetid: 8ADF4751-3BC5-4353-9927-C7E0079D0B83
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MFGetWorkQueueMMCSSPriority, MFGetWorkQueueMMCSSPriority function [Media Foundation], mf.mfgetworkqueuemmcsspriority, mfapi/MFGetWorkQueueMMCSSPriority, mfplat/MFGetWorkQueueMMCSSPriority
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
 - MFGetWorkQueueMMCSSPriority
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFGetWorkQueueMMCSSPriority function


## -description


Gets the relative thread priority of a work queue.


## -parameters




### -param dwWorkQueueId [in]

The identifier of the work queue. For private work queues, the identifier is returned by the <a href="https://msdn.microsoft.com/8def4375-919c-4619-9484-9ce2708a3886">MFAllocateWorkQueue</a> function. For platform work queues, see <a href="https://msdn.microsoft.com/c769f876-83ca-4b04-a054-22fa7146310e">Work Queue Identifiers</a>.


### -param lPriority [out]

Receives the relative thread priority.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function returns the relative thread priority set by the <a href="https://msdn.microsoft.com/D27E2B51-857D-48E5-8D25-A26917FCF959">MFBeginRegisterWorkQueueWithMMCSSEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/9E2A1D94-BF82-488E-8297-D524683ABE17">Work Queue and Threading Improvements</a>
 

 

