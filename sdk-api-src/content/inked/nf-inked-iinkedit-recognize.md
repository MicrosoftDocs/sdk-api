---
UID: NF:inked.IInkEdit.Recognize
title: IInkEdit::Recognize (inked.h)
description: Performs recognition on an InkStrokes collection and returns recognition results.
helpviewer_keywords: ["IInkEdit interface [Tablet PC]","Recognize method","IInkEdit.Recognize","IInkEdit::Recognize","Recognize","Recognize method [Tablet PC]","Recognize method [Tablet PC]","IInkEdit interface","e22043da-6c38-49e2-9651-43211ce7f377","inked/IInkEdit::Recognize","tablet.inkedit_recognize"]
old-location: tablet\inkedit_recognize.htm
tech.root: tablet
ms.assetid: e22043da-6c38-49e2-9651-43211ce7f377
ms.date: 12/05/2018
ms.keywords: IInkEdit interface [Tablet PC],Recognize method, IInkEdit.Recognize, IInkEdit::Recognize, Recognize, Recognize method [Tablet PC], Recognize method [Tablet PC],IInkEdit interface, e22043da-6c38-49e2-9651-43211ce7f377, inked/IInkEdit::Recognize, tablet.inkedit_recognize
f1_keywords:
- inked/IInkEdit.Recognize
dev_langs:
- c++
req.header: inked.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkEd.dll
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- InkEd.dll
- InkEd.dll.dll
api_name:
- IInkEdit.Recognize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkEdit::Recognize


## -description



Performs recognition on an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection and returns recognition results.




## -parameters






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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846764(v=VS.85).aspx">IInkEdit</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkedit-control-reference">InkEdit</a>
 

 

