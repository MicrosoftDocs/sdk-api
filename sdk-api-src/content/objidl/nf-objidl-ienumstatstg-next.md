---
UID: NF:objidl.IEnumSTATSTG.Next
title: IEnumSTATSTG::Next
author: windows-sdk-content
description: Retrieves a specified number of STATSTG structures, that follow in the enumeration sequence.
old-location: stg\ienumstatstg_next.htm
tech.root: stg
ms.assetid: 09363d3e-a606-4a50-8758-d7ef5b3c05ab
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumSTATSTG interface [Structured Storage],Next method, IEnumSTATSTG.Next, IEnumSTATSTG::Next, Next, Next method [Structured Storage], Next method [Structured Storage],IEnumSTATSTG interface, objidl/IEnumSTATSTG::Next, stg.ienumstatstg_next
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG.Next
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSTATSTG::Next


## -description


The <b>Next</b> method retrieves a specified number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures, that follow in the enumeration sequence. If there are fewer than the requested number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures that remain in the enumeration sequence, it retrieves the remaining <b>STATSTG</b> structures.


## -parameters




### -param celt [in]

The number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures requested.


### -param rgelt [out]

An array of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures returned.


### -param pceltFetched [out]

The number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures  retrieved in the <i>rgelt</i> parameter.


## -returns



This method supports the following return values:

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
The number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures returned is equal to the number specified in the <i>celt</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures returned is less than the number specified in the <i>celt</i> parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/93b8b14e-94e4-460b-9846-413affad8e4f">IEnumSTATSTG</a>
 

 

