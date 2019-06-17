---
UID: NF:oleauto.SafeArrayReleaseData
title: SafeArrayReleaseData function (oleauto.h)
author: windows-sdk-content
description: Decreases the pinning reference count for the specified safe array data by one. When that count reaches 0, the memory for that data is no longer prevented from being freed.
old-location: automat\safearrayreleasedata.htm
tech.root: automat
ms.assetid: AF3C36A3-2B3A-4159-8183-DB082FBFD215
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SafeArrayReleaseData, SafeArrayReleaseData function [Automation], automat.safearrayreleasedata, oleauto/SafeArrayReleaseData
ms.topic: function
f1_keywords: ["oleauto/SafeArrayReleaseData"]
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
 - SafeArrayReleaseData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



A call to the <b>SafeArrayReleaseData</b> function should match every previous call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayaddref">SafeArrayAddRef</a> function that returned a non-null value in the <i>ppDataToRelease</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayaddref">SafeArrayAddRef</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayreleasedescriptor">SafeArrayReleaseDescriptor</a>
 

 

