---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses
title: ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses
author: windows-driver-content
description: The EnumerateTerminalClasses method lists all terminal classes for the current terminal superclass.
old-location: tapi3\itpluggableterminalsuperclassregistration_enumerateterminalclasses.htm
old-project: Tapi
ms.assetid: dc75972d-7917-406d-8ed8-e05679ab86eb
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: EnumerateTerminalClasses, EnumerateTerminalClasses method [TAPI 2.2], EnumerateTerminalClasses method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],EnumerateTerminalClasses method, ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses, ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses, _tapi3_itpluggableterminalsuperclassregistration_enumerateterminalclasses, tapi3.itpluggableterminalsuperclassregistration_enumerateterminalclasses, termmgr/ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses
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
-	ITPluggableTerminalSuperclassRegistration.EnumerateTerminalClasses
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses


## -description


The 
<b>EnumerateTerminalClasses</b> method lists all terminal classes for the current terminal superclass.


## -parameters




### -param ppTerminals [out]

Pointer to the 
<a href="https://msdn.microsoft.com/1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe">IEnumTerminalClass</a> interface that enumerates the terminal classes.


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
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppTerminals</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe">IEnumTerminalClass</a> interface returned by <b>ITPluggableTerminalSuperclassRegistration::EnumerateTerminalClasses</b>. The application must call <b>Release</b> on the 
<b>IEnumTerminalClass</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/1da0a82a-fde4-440c-ac6c-e9b85a7ec3fe">IEnumTerminalClass</a>



<a href="https://msdn.microsoft.com/76f5d213-d1fb-4437-af09-9d915db05dc6">ITPluggableTerminalSuperclassRegistration</a>
 

 

