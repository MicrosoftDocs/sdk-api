---
UID: NF:oleauto.SafeArrayAddRef
title: SafeArrayAddRef function
author: windows-sdk-content
description: Increases the pinning reference count of the descriptor for the specified safe array by one, and may increase the pinning reference count of the data for the specified safe array by one if that data was dynamically allocated, as determined by the descriptor of the safe array.
old-location: automat\safearrayaddref.htm
tech.root: automat
ms.assetid: 0745D2E7-447E-4688-ADCF-1F889BC55BFB
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SafeArrayAddRef, SafeArrayAddRef function [Automation], automat.safearrayaddref, oleauto/SafeArrayAddRef
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
req.lib: Mincore.lib
req.dll: Oleaut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Oleaut32.dll
api_name:
 - SafeArrayAddRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayAddRef function


## -description


<div class="alert"><b>Note</b>  You should only call <b>SafeArrayAddRef</b> if you are implementing a scripting engine that needs to guard against running potentially malicious scripts.</div><div> </div>Increases the pinning reference count of the descriptor for the specified safe array by one, and may increase the pinning reference count of the data for the specified safe array by one if that data was dynamically allocated, as determined by the descriptor of the safe array.


## -parameters




### -param psa [in]

The safe array for which the pinning reference count of the descriptor should increase. While that count remains greater than 0, the memory for the descriptor is prevented from being freed by calls to the <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a> or <a href="https://msdn.microsoft.com/f1e8de45-673b-4f20-a639-18c724c82df1">SafeArrayDestroyDescriptor</a> functions.


### -param ppDataToRelease [out]

Returns the safe array data for which a pinning reference was added, if <b>SafeArrayAddRef</b> also added  a pinning reference for the  safe array data.  This parameter is NULL if <b>SafeArrayAddRef</b> did not add a pinning reference for the safe array data. <b>SafeArrayAddRef</b> does not add a pinning reference for the safe array data if that safe array data was not dynamically allocated.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Safe arrays have not traditionally had a reference count. All existing usage of safe arrays will continue to work with no changes. The <b>SafeArrayAddRef</b>, <a href="https://msdn.microsoft.com/AF3C36A3-2B3A-4159-8183-DB082FBFD215">SafeArrayReleaseData</a>, <a href="https://msdn.microsoft.com/D6678B17-B537-46CF-AC64-4D0C0DC4CDF3">SafeArrayReleaseDescriptor</a> functions add the ability to use reference counting to pin the safe array into memory before calling from an untrusted script into an <a href="https://msdn.microsoft.com/ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> method that may not expect the script to free that memory before the method returns, so that the script cannot force the code for that method into accessing memory that has been freed. After such a method safely returns, the pinning references should be released.   You can release the pinning references by calling the following functions:  

<ul>
<li>
<a href="https://msdn.microsoft.com/AF3C36A3-2B3A-4159-8183-DB082FBFD215">SafeArrayReleaseData</a>, for the data that the <i>ppDataToRelease</i> parameter points to, if it is not null.</li>
<li>
<a href="https://msdn.microsoft.com/D6678B17-B537-46CF-AC64-4D0C0DC4CDF3">SafeArrayReleaseDescriptor</a>, for the descriptor that the <i>psa</i> parameter specifies.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/AF3C36A3-2B3A-4159-8183-DB082FBFD215">SafeArrayReleaseData</a>



<a href="https://msdn.microsoft.com/D6678B17-B537-46CF-AC64-4D0C0DC4CDF3">SafeArrayReleaseDescriptor</a>
 

 

