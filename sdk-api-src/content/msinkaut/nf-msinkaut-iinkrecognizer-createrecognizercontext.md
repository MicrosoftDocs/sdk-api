---
UID: NF:msinkaut.IInkRecognizer.CreateRecognizerContext
title: IInkRecognizer::CreateRecognizerContext
author: windows-sdk-content
description: Creates a new InkRecognizerContext object.
old-location: tablet\iinkrecognizer_createrecognizercontext.htm
old-project: tablet
ms.assetid: b6aeec3f-8d57-4667-b171-1d8cad95f45c
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: CreateRecognizerContext, CreateRecognizerContext method [Tablet PC], CreateRecognizerContext method [Tablet PC],IInkRecognizer interface, IInkRecognizer interface [Tablet PC],CreateRecognizerContext method, IInkRecognizer.CreateRecognizerContext, IInkRecognizer::CreateRecognizerContext, b6aeec3f-8d57-4667-b171-1d8cad95f45c, msinkaut/IInkRecognizer::CreateRecognizerContext, tablet.iinkrecognizer_createrecognizercontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
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
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizer.CreateRecognizerContext
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognizer::CreateRecognizerContext


## -description



Creates a new <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> object.




## -parameters




### -param Context [out, retval]

Returns a <a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext</a> for the invoking <a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

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




<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

