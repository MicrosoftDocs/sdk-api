---
UID: NF:chstrarr.CHStringArray.RemoveAll
title: CHStringArray::RemoveAll
author: windows-sdk-content
description: The RemoveAll method removes all the CHString members from this array.
old-location: wmi\chstringarray_removeall.htm
old-project: WmiSdk
ms.assetid: be9df3fd-afa5-4f07-99cd-ddccdeaa3fd3
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: CHStringArray interface [Windows Management Instrumentation],RemoveAll method, CHStringArray.RemoveAll, CHStringArray::RemoveAll, RemoveAll, RemoveAll method [Windows Management Instrumentation], RemoveAll method [Windows Management Instrumentation],CHStringArray interface, _hmm_chstringarray_removeall, chstrarr/CHStringArray::RemoveAll, wmi.chstringarray_removeall
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: chstrarr.h
req.include-header: FwCommon.h
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
 - CHStringArray.RemoveAll
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::RemoveAll


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>RemoveAll</b> method removes all the <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> members from this array.


## -parameters






## -returns



This method does not return a value.




## -remarks



The <b>RemoveAll</b> method works on empty arrays.


#### Examples

The following code example shows the use of <b>CHStringArray::RemoveAll</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHStringArray array;

array.Add( L"String 1" ); // Element 0
array.Add( L"String 2" ); // Element 1 
assert( array.GetSize() == 2 ); 
array.RemoveAll(); 
assert( array.GetSize() == 0 );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/5ed54cc4-284b-4cd7-80c1-e9c5ff27c4bf">CHStringArray::FreeExtra</a>
 

 

