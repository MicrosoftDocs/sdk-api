---
UID: NF:tom.ITextRow.GetCellColorFore
title: ITextRow::GetCellColorFore
author: windows-sdk-content
description: Gets the foreground color of the active cell.
old-location: controls\itextrow_getcellcolorfore.htm
old-project: Controls
ms.assetid: 92c8bff3-a56b-4adc-9f49-728f22c1089b
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetCellColorFore, GetCellColorFore method [Windows Controls], GetCellColorFore method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellColorFore method, ITextRow.GetCellColorFore, ITextRow::GetCellColorFore, controls.itextrow_getcellcolorfore, tom/ITextRow::GetCellColorFore
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRow.GetCellColorFore
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRow::GetCellColorFore


## -description


Gets the foreground color of the active cell.


## -parameters




### -param pValue [out, retval]

Type: <b>long*</b>

The foreground color.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns the following COM error code. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>



<a href="https://msdn.microsoft.com/2eff9f39-b79d-4fcb-b8ee-ef067cff2c78">ITextRow::SetCellColorFore</a>
 

 

