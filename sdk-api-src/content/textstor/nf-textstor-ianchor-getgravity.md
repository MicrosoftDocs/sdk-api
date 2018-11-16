---
UID: NF:textstor.IAnchor.GetGravity
title: IAnchor::GetGravity
author: windows-sdk-content
description: The IAnchor::GetGravity method retrieves the gravity of the anchor in an IAnchor object.
old-location: tsf\ianchor_getgravity.htm
tech.root: TSF
ms.assetid: c56a4c25-ac43-4fd3-8d6b-943eb0233ed4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetGravity, GetGravity method [Text Services Framework], GetGravity method [Text Services Framework],IAnchor interface, IAnchor interface [Text Services Framework],GetGravity method, IAnchor.GetGravity, IAnchor::GetGravity, textstor/IAnchor::GetGravity, tsf.ianchor_getgravity
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
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IAnchor.GetGravity
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- textstor.h
: 
- IAnchor.GetGravity
: 
---

# IAnchor::GetGravity


## -description


The <b>IAnchor::GetGravity</b> method retrieves the gravity of the anchor in an <a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a> object.


## -parameters




### -param pgravity [out]

Pointer that receives a <a href="https://msdn.microsoft.com/12ec85b9-e65f-485d-8e42-164d2a988356">TsGravity</a> value that specifies the anchor gravity.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pgravity</i> pointer is invalid. 

</td>
</tr>
</table>
 




## -see-also




<a href="ranges.htm">Anchor Gravity</a>



<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/c532abcf-9ae0-4566-80f7-0bb4ae908fce">IAnchor::SetGravity</a>



<a href="https://msdn.microsoft.com/12ec85b9-e65f-485d-8e42-164d2a988356">TsGravity</a>
 

 

