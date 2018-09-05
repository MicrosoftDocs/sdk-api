---
UID: NF:infotech.IITPropList.Get
title: IITPropList::Get
author: windows-sdk-content
description: Returns the property object associated with the given property ID.
old-location: htmlhelp\iitproplist_get.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistget.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: Get, Get method [HTML Help Workshop], Get method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],Get method, IITPropList.Get, IITPropList::Get, htmlhelp.iitproplist_get, infotech/IITPropList::Get, refIITPropListGet
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: infotech.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITPropList.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITPropList::Get


## -description


Returns the property object associated with the given property ID.




## -parameters




### -param PropID [in]

ID of the property object to get.




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
 

 

