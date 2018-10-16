---
UID: NF:tom.ITextRow.Apply
title: ITextRow::Apply
author: windows-sdk-content
description: Applies the formatting attributes of this text row object to the specified rows in the associated ITextRange2.
old-location: controls\itextrow_apply.htm
tech.root: controls
ms.assetid: f09f73d3-c71f-43f1-b671-aba392e1fb49
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: Apply, Apply method [Windows Controls], Apply method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],Apply method, ITextRow.Apply, ITextRow::Apply, controls.itextrow_apply, tom/ITextRow::Apply, tomCellStructureChangeOnly, tomRowApplyDefault
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
 - ITextRow.Apply
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRow::Apply


## -description


Applies the formatting attributes of this text row object to the specified rows in the associated <a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>.


## -parameters




### -param cRow [in]

Type: <b>long</b>

The number of rows to apply this text row object to.


### -param Flags [in]

Type: <b>long</b>

A flag that controls how the formatting attributes are applied. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomCellStructureChangeOnly"></a><a id="tomcellstructurechangeonly"></a><a id="TOMCELLSTRUCTURECHANGEONLY"></a><dl>
<dt><b>tomCellStructureChangeOnly</b></dt>
</dl>
</td>
<td width="60%">
Apply formatting attributes only to cell widths or the cell count (enables you to change column widths or insert/delete columns without changing other properties, such as cell borders).

</td>
</tr>
<tr>
<td width="40%"><a id="tomRowApplyDefault"></a><a id="tomrowapplydefault"></a><a id="TOMROWAPPLYDEFAULT"></a><dl>
<dt><b>tomRowApplyDefault</b></dt>
</dl>
</td>
<td width="60%">
Apply formatting attributes to the full application, not just cell widths and count.

</td>
</tr>
</table>
 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/49f5ffc1-d615-4d07-9f41-1c5f0dd9045b">ITextRow</a>
 

 

