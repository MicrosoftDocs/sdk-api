---
UID: NF:inked.IInkEdit.Recognize
title: IInkEdit::Recognize
author: windows-sdk-content
description: Performs recognition on an InkStrokes collection and returns recognition results.
old-location: tablet\inkedit_recognize.htm
old-project: tablet
ms.assetid: e22043da-6c38-49e2-9651-43211ce7f377
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: IInkEdit interface [Tablet PC],Recognize method, IInkEdit.Recognize, IInkEdit::Recognize, Recognize, Recognize method [Tablet PC], Recognize method [Tablet PC],IInkEdit interface, e22043da-6c38-49e2-9651-43211ce7f377, inked/IInkEdit::Recognize, tablet.inkedit_recognize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SelAlignmentConstants
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
product: Windows
targetos: Windows
req.lib: InkEd.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IInkEdit::Recognize


## -description



Performs recognition on an <a href="https://msdn.microsoft.com/c7fb921c-0bd2-48aa-b092-ab1fb08c0697">InkStrokes</a> collection and returns recognition results.




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




<a href="tablet.iinkedit_">IInkEdit</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>
 

 

