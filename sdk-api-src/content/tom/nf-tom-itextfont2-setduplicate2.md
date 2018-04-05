---
UID: NF:tom.ITextFont2.SetDuplicate2
title: ITextFont2::SetDuplicate2 method
author: windows-driver-content
description: Sets the properties of this object by copying the properties of another text font object.
old-location: controls\itextfont2_setduplicate2.htm
old-project: Controls
ms.assetid: aaaafed9-be20-40a2-beed-09703970452f
ms.author: windowsdriverdev
ms.date: 3/31/2018
ms.keywords: ITextFont2, ITextFont2 interface [Windows Controls], SetDuplicate2 method, ITextFont2::SetDuplicate2, SetDuplicate2 method [Windows Controls], SetDuplicate2 method [Windows Controls], ITextFont2 interface, SetDuplicate2,ITextFont2.SetDuplicate2, controls.itextfont2_setduplicate2, tom/ITextFont2::SetDuplicate2
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
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.SetDuplicate2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::SetDuplicate2 method


## -description


Sets the properties of this object by copying the properties of another text font object.


## -parameters




### -param pFont [in]

Type: <b><a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>*</b>

The text font object to copy from.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes.  For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



Values with the <b>tomUndefined</b> attribute have no effect.

For an example of how to use font duplicates, see <a href="https://msdn.microsoft.com/15630fec-83b2-4169-b141-8ce253dd25fe">ITextRange::SetFont</a>.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/dc6b979b-f837-4945-a35d-c5585d703bd1">ITextFont2::GetDuplicate2</a>
 

 

