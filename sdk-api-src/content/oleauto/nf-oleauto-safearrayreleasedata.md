---
UID: NF:oleauto.SafeArrayReleaseData
title: SafeArrayReleaseData function
author: windows-sdk-content
description: Decreases the pinning reference count for the specified safe array data by one. When that count reaches 0, the memory for that data is no longer prevented from being freed.
old-location: automat\safearrayreleasedata.htm
old-project: automat
ms.assetid: AF3C36A3-2B3A-4159-8183-DB082FBFD215
ms.author: windowssdkdev
ms.date: 05/07/2018
ms.keywords: SafeArrayReleaseData, SafeArrayReleaseData function [Automation], automat.safearrayreleasedata, oleauto/SafeArrayReleaseData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - SafeArrayReleaseData
product: Windows
targetos: Windows
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
req.product: ADAM
---

# SafeArrayReleaseData function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SafeArrayReleaseData</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the specified safe array data by one. When that count reaches 0, the memory for that data is no longer prevented from being freed.


## -parameters




### -param pData [in]

The safe array data for which the pinning reference count should decrease.


## -returns



This function does not return a value.




## -remarks



A call to the <b>SafeArrayReleaseData</b> function should match every previous call to the <a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a> function that returned a non-null value in the <i>ppDataToRelease</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a>



<a href="https://msdn.microsoft.com/D6678B17-B537-46CF-AC64-4D0C0DC4CDF3">SafeArrayReleaseDescriptor</a>
 

 

