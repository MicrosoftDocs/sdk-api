---
UID: NF:tapi3if.ITCallHub.EnumerateCalls
title: ITCallHub::EnumerateCalls
author: windows-sdk-content
description: The EnumerateCalls method enumerates calls currently associated with the call hub. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Calls method.
old-location: tapi3\itcallhub_enumeratecalls.htm
old-project: Tapi
ms.assetid: becacf70-0ae7-419c-a53f-c6172278d29f
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: EnumerateCalls, EnumerateCalls method [TAPI 2.2], EnumerateCalls method [TAPI 2.2],ITCallHub interface, ITCallHub interface [TAPI 2.2],EnumerateCalls method, ITCallHub.EnumerateCalls, ITCallHub::EnumerateCalls, _tapi3_itcallhub_enumeratecalls, tapi3.itcallhub_enumeratecalls, tapi3if/ITCallHub::EnumerateCalls
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TERMINAL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITCallHub.EnumerateCalls
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITCallHub::EnumerateCalls


## -description


The 
<b>EnumerateCalls</b> method enumerates calls currently associated with the call hub. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/56634ab6-b905-48bb-a4d1-7ca1f0c4c0cf">get_Calls</a> method.


## -parameters




### -param ppEnumCall [out]

Pointer to 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create the enumerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumCall</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/418c1005-98f0-406f-a85c-c08adb269b9f">IEnumCall</a> interface returned by <b>ITCallHub::EnumerateCalls</b>. The application must call <b>Release</b> on the 
<b>IEnumCall</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/ea23ae25-2fbb-4060-8273-cd7921d49e52">CallHub Object</a>



<a href="https://msdn.microsoft.com/bdc91cac-c0ec-4484-a415-8cd1aa1e18e8">ITCallHub</a>
 

 

