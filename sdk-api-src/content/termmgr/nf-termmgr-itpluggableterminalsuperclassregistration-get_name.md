---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.get_Name
title: ITPluggableTerminalSuperclassRegistration::get_Name
author: windows-sdk-content
description: The get_Name method gets the friendly name for the terminal superclass.
old-location: tapi3\itpluggableterminalsuperclassregistration_get_name.htm
tech.root: Tapi
ms.assetid: 42f58ac2-4fda-436c-bbfd-d339296f736e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],get_Name method, ITPluggableTerminalSuperclassRegistration.get_Name, ITPluggableTerminalSuperclassRegistration::get_Name, _tapi3_itpluggableterminalsuperclassregistration_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_get_name, termmgr/ITPluggableTerminalSuperclassRegistration::get_Name
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
req.include-header: 
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassRegistration.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalSuperclassRegistration::get_Name


## -description


The 
<b>get_Name</b> method gets the friendly name for the terminal superclass.


## -parameters




### -param pName [out]

 Pointer to a <b>BSTR</b> representation of the friendly name. The <b>BSTR</b> is allocated using 
<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>



<a href="https://msdn.microsoft.com/fe9b569b-bfb7-401b-98a8-5db7f3739d41">put_Name</a>
 

 

