---
UID: NF:infotech.IITPropList.GetFirst
title: IITPropList::GetFirst
author: windows-driver-content
description: Returns the first property object in a property list.
old-location: htmlhelp\iitproplist_getfirst.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistgetfirst.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetFirst, GetFirst method [HTML Help Workshop], GetFirst method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],GetFirst method, IITPropList.GetFirst, IITPropList::GetFirst, htmlhelp.iitproplist_getfirst, infotech/IITPropList::GetFirst, refIITPropListGetFirst
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITPropList.GetFirst
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITPropList::GetFirst


## -description


Returns the first property object in a property list.




## -parameters




### -param Property [out, ref]

The property object returned.




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
The property was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTEXIST</b></dt>
</dl>
</td>
<td width="60%">
The requested property does not exist.



</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/09200749-bd1d-4266-895e-29e21525bac2">IITPropList</a>
 

 

