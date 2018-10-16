---
UID: NF:tom.ITextRange2.GetSubrange
title: ITextRange2::GetSubrange
author: windows-sdk-content
description: Retrieves a subrange in a range.
old-location: controls\itextrange2_getsubrange.htm
tech.root: controls
ms.assetid: 64b031cf-9d32-4e36-8e13-f32a53f00abf
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetSubrange, GetSubrange method [Windows Controls], GetSubrange method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetSubrange method, ITextRange2.GetSubrange, ITextRange2::GetSubrange, controls.itextrange2_getsubrange, tom/ITextRange2::GetSubrange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msftedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange2.GetSubrange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRange2::GetSubrange


## -description


Retrieves a subrange in a range.


## -parameters




### -param iSubrange [in]

Type: <b>long</b>

The subrange index.


### -param pcpFirst [out]

Type: <b>long*</b>

The character position for the start of the subrange.


### -param pcpLim [out]

Type: <b>long*</b>

The character position for the end of the subrange.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Subranges are selected as follows.<table>
<tr>
<th>iSubrange value</th>
<th>Subrange</th>
</tr>
<tr>
<td>Equals zero</td>
<td>Gets the current active subrange.</td>
</tr>
<tr>
<td>Greater than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in the order in which the subranges were added. This requires extra calculation.</td>
</tr>
<tr>
<td>Less than zero</td>
<td>Gets the subrange at the index specified by <i>iSubrange</i>, in increasing character position order.</td>
</tr>
</table>
 



See <a href="https://msdn.microsoft.com/a1744e60-74b0-44a0-b470-6e89d328fa11">ITextRange2::GetCount</a> for the count of subranges not including the active subrange.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

