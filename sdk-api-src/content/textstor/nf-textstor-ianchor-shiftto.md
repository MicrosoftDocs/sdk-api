---
UID: NF:textstor.IAnchor.ShiftTo
title: IAnchor::ShiftTo
author: windows-driver-content
description: The IAnchor::ShiftTo method shifts the current anchor to the same position as another anchor.
old-location: tsf\ianchor_shiftto.htm
old-project: TSF
ms.assetid: a0fb9a08-3f46-4d2f-8887-e80dc0bade1b
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IAnchor interface [Text Services Framework],ShiftTo method, IAnchor.ShiftTo, IAnchor::ShiftTo, ShiftTo, ShiftTo method [Text Services Framework], ShiftTo method [Text Services Framework],IAnchor interface, textstor/IAnchor::ShiftTo, tsf.ianchor_shiftto
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	IAnchor.ShiftTo
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAnchor::ShiftTo


## -description


The <b>IAnchor::ShiftTo</b> method shifts the current anchor to the same position as another anchor.


## -parameters




### -param paSite [in]

Anchor occupying a position that the current anchor will be moved to.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An <a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a> interface pointer to the <i>paSite</i> anchor could not be obtained, or memory is too low to safely complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paSite</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Implementing this method is usually more efficient than an equivalent <a href="https://msdn.microsoft.com/e57a78e6-42e6-4a2b-b4e1-20bb64add872">IAnchor::Shift</a> operation.




## -see-also




<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/e57a78e6-42e6-4a2b-b4e1-20bb64add872">IAnchor::Shift
      </a>
 

 

