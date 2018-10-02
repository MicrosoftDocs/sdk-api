---
UID: NF:tom.ITextRow.Reset
title: ITextRow::Reset
author: windows-sdk-content
description: Resets a row.
old-location: controls\itextrow_reset.htm
tech.root: controls
ms.assetid: 49f057ba-6376-496b-b0b0-97c6a00111c4
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ITextRow interface [Windows Controls],Reset method, ITextRow.Reset, ITextRow::Reset, Reset, Reset method [Windows Controls], Reset method [Windows Controls],ITextRow interface, controls.itextrow_reset, tom/ITextRow::Reset
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
 - ITextRow.Reset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::Reset


## -description


Resets a row.


## -parameters




### -param Value [in]

Type: <b>long</b>

The <a href="https://msdn.microsoft.com/en-us/library/Hh768766(v=VS.85).aspx">tomRowUpdate</a> reset value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>
 

 

