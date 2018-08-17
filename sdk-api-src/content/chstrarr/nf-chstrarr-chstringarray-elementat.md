---
UID: NF:chstrarr.CHStringArray.ElementAt
title: CHStringArray::ElementAt
author: windows-sdk-content
description: The ElementAt method returns a temporary reference to the element pointer within the array.
old-location: wmi\chstringarray_elementat.htm
old-project: WmiSdk
ms.assetid: 5431a9ae-e009-4457-87e4-bb91da8bfdb6
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],ElementAt method, CHStringArray.ElementAt, CHStringArray::ElementAt, ElementAt, ElementAt method [Windows Management Instrumentation], ElementAt method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_elementat, chstrarr/CHStringArray::ElementAt, wmi.chstringarray_elementat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstrarr.h
req.include-header: FwCommon.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FrameDynOS.dll
 - FrameDyn.dll
api_name:
 - CHStringArray.ElementAt
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::ElementAt


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/en-us/library/JJ152383(v=VS.85).aspx">MI APIs</a> should be used for all new 
    development.]

The <b>ElementAt</b> method returns a temporary reference to the element pointer within the array.


## -parameters




### -param nIndex

An integer index that is greater than or equal to zero and less than or equal to the value returned by <a href="https://msdn.microsoft.com/en-us/library/Aa385377(v=VS.85).aspx">GetUpperBound</a>.


## -returns



If the <b>ElementAt</b> method is successful, it returns a reference to the <a href="https://msdn.microsoft.com/en-us/library/Aa384937(v=VS.85).aspx">CHString</a> string at the <i>nIndex</i> position in the <a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a> array.




## -remarks



Use the <b>ElementAt</b> method to implement the left-side assignment operator for arrays. This is an advanced method, which you should use only to implement special array operators.


#### Examples

See the example for <a href="https://msdn.microsoft.com/en-us/library/Aa385370(v=VS.85).aspx">CHStringArray::GetSize</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385304(v=VS.85).aspx">CHStringArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385363(v=VS.85).aspx">CHStringArray::GetAt</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385367(v=VS.85).aspx">CHStringArray::GetData</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385402(v=VS.85).aspx">CHStringArray::SetAt</a>
 

 

