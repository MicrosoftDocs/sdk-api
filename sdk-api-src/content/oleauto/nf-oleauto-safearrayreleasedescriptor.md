---
UID: NF:oleauto.SafeArrayReleaseDescriptor
title: SafeArrayReleaseDescriptor function
author: windows-driver-content
description: Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed.
old-location: automat\safearrayreleasedescriptor.htm
old-project: automat
ms.assetid: D6678B17-B537-46CF-AC64-4D0C0DC4CDF3
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: SafeArrayReleaseDescriptor, SafeArrayReleaseDescriptor function [Automation], automat.safearrayreleasedescriptor, oleauto/SafeArrayReleaseDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Oleaut32.dll
api_name:
-	SafeArrayReleaseDescriptor
product: Windows
targetos: Windows
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SafeArrayReleaseDescriptor function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SafeArrayReleaseDescriptor</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Decreases the pinning reference count for the descriptor of the specified safe array by one. When that count reaches 0, the memory for that descriptor is no longer prevented from being freed.


## -parameters




### -param psa [in]

The safe array for which the pinning reference count of the descriptor should decrease.


## -returns



This function does not return a value.




## -remarks



A call to the <b>SafeArrayReleaseDescriptor</b> function should match every previous call to the <a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0745D2E7-447E-4688-ADCF-1F889BC55BFB">SafeArrayAddRef</a>



<a href="https://msdn.microsoft.com/AF3C36A3-2B3A-4159-8183-DB082FBFD215">SafeArrayReleaseData</a>
 

 

