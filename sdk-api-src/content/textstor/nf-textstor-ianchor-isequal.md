---
UID: NF:textstor.IAnchor.IsEqual
title: IAnchor::IsEqual
author: windows-sdk-content
description: The IAnchor::IsEqual method evaluates two anchors within a text stream and returns a Boolean value that specifies the equality or inequality of the anchor positions.
old-location: tsf\ianchor_isequal.htm
tech.root: TSF
ms.assetid: a2dedce7-f64d-406a-bebc-9a4b51a1ae38
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IAnchor interface [Text Services Framework],IsEqual method, IAnchor.IsEqual, IAnchor::IsEqual, IsEqual, IsEqual method [Text Services Framework], IsEqual method [Text Services Framework],IAnchor interface, textstor/IAnchor::IsEqual, tsf.ianchor_isequal
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
 - IAnchor.IsEqual
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
- IAnchor.IsEqual
: 
---

# IAnchor::IsEqual


## -description


The <b>IAnchor::IsEqual</b> method evaluates two anchors within a text stream and returns a Boolean value that specifies the equality or inequality of the anchor positions.


## -parameters




### -param paWith [in]

Specifies an anchor to compare to the primary anchor. Used to determine the equality of the two anchor positions.


### -param pfEqual [out]

A Boolean value that specifies whether the two anchors are positioned at the same location. If set to <b>TRUE</b>, the two anchors occupy the same location. If set to <b>FALSE</b>, the two anchors do not occupy the same location.


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
<i>pfEqual</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Anchors are always positioned between characters or regions. When two anchors are between the same characters, being at the same offset within the text stream, and within the same region, <b>IAnchor::IsEqual</b> returns <b>TRUE</b>. Otherwise it returns <b>FALSE</b>.


<a href="https://msdn.microsoft.com/227ed0c0-0bdd-49af-b5dc-fdb69913b9c1">IAnchor::Compare
        </a> incorporates the same functionality as <b>IAnchor::IsEqual</b>. However, because <b>IAnchor::IsEqual</b> is more specific, it can have a more efficient implementation on the server.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms629023(v=VS.85).aspx">Anchors</a>



<a href="https://msdn.microsoft.com/a7d52959-8386-464f-958d-c870f286b265">IAnchor</a>



<a href="https://msdn.microsoft.com/227ed0c0-0bdd-49af-b5dc-fdb69913b9c1">IAnchor::Compare
      </a>
 

 

