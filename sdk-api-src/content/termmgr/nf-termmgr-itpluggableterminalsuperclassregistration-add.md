---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.Add
title: ITPluggableTerminalSuperclassRegistration::Add method
author: windows-driver-content
description: The Add method adds a pluggable terminal superclass to the registry. If the superclass already exists, the method modifies the information for the superclass.
old-location: tapi3\itpluggableterminalsuperclassregistration_add.htm
old-project: Tapi
ms.assetid: ffef0255-c262-43d4-905f-5574c205c37e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: Add method [TAPI 2.2], Add method [TAPI 2.2], ITPluggableTerminalSuperclassRegistration interface, Add,ITPluggableTerminalSuperclassRegistration.Add, ITPluggableTerminalSuperclassRegistration, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2], Add method, ITPluggableTerminalSuperclassRegistration::Add, _tapi3_itpluggableterminalsuperclassregistration_add, tapi3.itpluggableterminalsuperclassregistration_add, termmgr/ITPluggableTerminalSuperclassRegistration::Add
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
-	ITPluggableTerminalSuperclassRegistration.Add
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalSuperclassRegistration::Add method


## -description


The 
<b>Add</b> method adds a pluggable terminal superclass to the registry. If the superclass already exists, the method modifies the information for the superclass.


## -parameters






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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>
 




## -remarks



The 
<b>Add</b> method adds a new terminal superclass if the CLSID does not exist as an entry in the registry. The method modifies the information about a terminal superclass if the CLSID already exists in the registry.

If the CLSID for the terminal superclass was not set for terminal superclass, the 
<b>Add</b> method fails.




## -see-also




<a href="https://msdn.microsoft.com/fe87d55f-1e1c-4241-b8a3-b56d2000f3ca">Delete</a>



<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>
 

 

