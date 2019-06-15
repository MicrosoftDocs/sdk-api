---
UID: NF:tom.ITextRow.Reset
title: ITextRow::Reset (tom.h)
author: windows-sdk-content
description: Resets a row.
old-location: controls\itextrow_reset.htm
tech.root: Controls
ms.assetid: 49f057ba-6376-496b-b0b0-97c6a00111c4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],Reset method, ITextRow.Reset, ITextRow::Reset, Reset, Reset method [Windows Controls], Reset method [Windows Controls],ITextRow interface, controls.itextrow_reset, tom/ITextRow::Reset
ms.topic: method
f1_keywords: ["tom/ITextRow.Reset"]
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
ms.custom: 19H1
---

# ITextRow::Reset


## -description


Resets a row.


## -parameters




### -param Value [in]

Type: <b>long</b>

The <a href="https://docs.microsoft.com/windows/desktop/api/tom/ne-tom-__midl___midl_itf_tom_0000_0000_0001">tomRowUpdate</a> reset value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://docs.microsoft.com/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

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




<a href="https://docs.microsoft.com/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>
 

 

