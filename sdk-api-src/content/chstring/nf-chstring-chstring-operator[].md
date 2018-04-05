---
UID: NF:chstring.CHString.operator[]
title: CHString::operator[] method
author: windows-driver-content
description: The overloaded subscript ([]) operator returns a single character specified by the zero-based index in nIndex. This operator is a convenient substitute for the GetAt method.
old-location: wmi\chstring__operator_brackets.htm
old-project: WmiSdk
ms.assetid: 9a0ba1f3-e862-4210-86a4-55a573e8bb4b
ms.author: windowsdriverdev
ms.date: 3/16/2018
ms.keywords: "??ACHString@@QBEGH@Z, ??ACHString@@QEBAGH@Z, CHString, CHString interface [Windows Management Instrumentation], operator [] method, CHString::operator [], CHString::operator[], chstring/CHString::operator [], operator [] method [Windows Management Instrumentation], operator [] method [Windows Management Instrumentation], CHString interface, operator[],CHString.operator[], wmi.chstring__operator_brackets"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: chstring.h
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
req.typenames: CF_SYNC_ROOT_STANDARD_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	FrameDynOS.dll
-	FrameDyn.dll
api_name:
-	CHString.operator []
-	??ACHString@@QBEGH@Z
-	??ACHString@@QEBAGH@Z
product: Windows
targetos: Windows
req.lib: FrameDyn.lib
req.dll: FrameDynOS.dll; FrameDyn.dll
req.irql: 
---

# CHString::operator[] method


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The overloaded subscript ([]) operator returns a single character specified by the zero-based index in <i>nIndex</i>. This operator is a convenient substitute for the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406567">GetAt</a> method.


## -parameters




### -param nIndex

Zero-based index of a character in the string.


## -remarks



<div class="alert"><b>Important</b>  You can use the subscript ([]) operator to get the value of a character in a <a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a> string, but you cannot use it to change the value of a character in a <b>CHString</b> string.</div>
<div> </div>

#### Examples

The following code example shows the use of <b>CHString::operator[]</b>:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CHString s( L"abc" );
assert( s[1] == 'b' );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e2e4378f-d842-4bca-bffc-a60e718caed3">CHString</a>



<a href="https://msdn.microsoft.com/ed038b41-211c-4483-99cd-0bc43b241761">CHString::GetAt</a>
 

 

