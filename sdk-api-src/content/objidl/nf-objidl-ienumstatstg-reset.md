---
UID: NF:objidl.IEnumSTATSTG.Reset
title: IEnumSTATSTG::Reset
author: windows-driver-content
description: Resets the enumeration sequence to the beginning of the STATSTG structure array.
old-location: stg\ienumstatstg_reset.htm
old-project: Stg
ms.assetid: 696aaa93-1b56-4baf-a6be-753c7d6f5456
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IEnumSTATSTG interface [Structured Storage],Reset method, IEnumSTATSTG.Reset, IEnumSTATSTG::Reset, Reset, Reset method [Structured Storage], Reset method [Structured Storage],IEnumSTATSTG interface, objidl/IEnumSTATSTG::Reset, stg.ienumstatstg_reset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IEnumSTATSTG.Reset
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumSTATSTG::Reset


## -description


The <b>Reset</b> method resets the enumeration sequence to the beginning of the <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure array.


## -parameters






## -returns



This method supports the S_OK return value.

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
The enumeration sequence was successfully reset to the beginning of the enumeration.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>
 

 

