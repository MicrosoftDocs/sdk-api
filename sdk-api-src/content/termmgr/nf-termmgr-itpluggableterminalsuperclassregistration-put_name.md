---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.put_Name
title: ITPluggableTerminalSuperclassRegistration::put_Name method
author: windows-driver-content
description: The put_Name method sets the friendly name for the terminal superclass.
old-location: tapi3\itpluggableterminalsuperclassregistration_put_name.htm
old-project: Tapi
ms.assetid: fe9b569b-bfb7-401b-98a8-5db7f3739d41
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2], put_Name method, ITPluggableTerminalSuperclassRegistration::put_Name, _tapi3_itpluggableterminalsuperclassregistration_put_name, put_Name method [TAPI 2.2], put_Name method [TAPI 2.2], ITPluggableTerminalSuperclassRegistration interface, put_Name,ITPluggableTerminalSuperclassRegistration.put_Name, tapi3.itpluggableterminalsuperclassregistration_put_name, termmgr/ITPluggableTerminalSuperclassRegistration::put_Name
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITPluggableTerminalSuperclassRegistration.put_Name
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalSuperclassRegistration::put_Name method


## -description


The 
<b>put_Name</b> method sets the friendly name for the terminal superclass.


## -parameters




### -param bstrName [in]

The <b>BSTR</b> representation of the friendly name.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>bstrName</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>



<a href="https://msdn.microsoft.com/42f58ac2-4fda-436c-bbfd-d339296f736e">get_Name</a>
 

 

