---
UID: NF:chstrarr.CHStringArray.Add
title: CHStringArray::Add
author: windows-driver-content
description: The Add method adds a new element to the end of an array, increasing the array by one.
old-location: wmi\chstringarray_add.htm
old-project: WmiSdk
ms.assetid: f5a0b8e6-b40a-4dc7-bf36-ec629e2899db
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: "?Add@CHStringArray@@QAEHPBG@Z, ?Add@CHStringArray@@QEAAHPEBG@Z, Add, Add method [Windows Management Instrumentation], Add method [Windows Management Instrumentation],CHStringArray interface, CHStringArray interface [Windows Management Instrumentation],Add method, CHStringArray.Add, CHStringArray::Add, _hmm_chstringarray_add, chstrarr/CHStringArray::Add, wmi.chstringarray_add"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CONFLICT_DETAILS_W, *PCONFLICT_DETAILS_W
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHStringArray.Add
-	?Add@CHStringArray@@QAEHPBG@Z
-	?Add@CHStringArray@@QEAAHPEBG@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHStringArray::Add


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Add</b> method adds a new element to the end of an 
    array, increasing the array by one.


## -parameters




### -param newElement

The element to be added to the array.


## -returns



If the <b>Add</b> method is successful, it returns the 
       index of the added element.




## -remarks



If <a href="https://msdn.microsoft.com/library/windows/hardware/hh439729">SetSize</a> has been used with an nGrowBy value 
    greater than 1, then extra memory can be allocated. However, the upper bound increases by only one.


#### Examples

The following code example shows the use of 
     <b>Add</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    CHStringArray array;
    CHString s( L"String 2");
    
    array.Add( L"String 1" ); // Element 0
    array.Add( s );           // Element 1</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/62959345-4fed-4107-b155-1746ad35c658">CHStringArray</a>



<a href="https://msdn.microsoft.com/c37df3d4-9b0b-4ed3-ab51-407f26203578">CHStringArray::Append</a>



<a href="https://msdn.microsoft.com/9598340f-c315-4c93-bc8a-2b7c1eaf5a35">CHStringArray::Copy</a>
 

 

