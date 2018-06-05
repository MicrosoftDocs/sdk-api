---
UID: NF:infotech.IITWordWheel.Count
title: IITWordWheel::Count
author: windows-sdk-content
description: Returns the number of entries in a word wheel.
old-location: htmlhelp\iitwordwheel_count.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheelcount.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Count, Count method [HTML Help Workshop], Count method [HTML Help Workshop],IITWordWheel interface, IITWordWheel interface [HTML Help Workshop],Count method, IITWordWheel.Count, IITWordWheel::Count, htmlhelp.iitwordwheel_count, infotech/IITWordWheel::Count, refIITWordWheelCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: infotech.h
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
tech.root: 
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITWordWheel.Count
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITWordWheel::Count


## -description


Returns the number of entries in a word wheel.




## -parameters




### -param pcEntries [in]

Number of entries in word wheel.




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
The count was successfully returned.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTOPEN</b></dt>
</dl>
</td>
<td width="60%">
The word wheel has not been opened.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pcEntries</i> parameter was an invalid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9734c73e-9325-4a6d-bbf3-3f87f96a662e">IITWordWheel</a>
 

 

