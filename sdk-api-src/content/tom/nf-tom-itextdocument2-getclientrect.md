---
UID: NF:tom.ITextDocument2.GetClientRect
title: ITextDocument2::GetClientRect
author: windows-sdk-content
description: Retrieves the client rectangle of the rich edit control.
old-location: controls\itextdocument2_getclientrect.htm
old-project: Controls
ms.assetid: a5736c58-e402-421d-aa4a-79b65460b692
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetClientRect, GetClientRect method [Windows Controls], GetClientRect method [Windows Controls],ITextDocument2 interface, ITextDocument2 interface [Windows Controls],GetClientRect method, ITextDocument2.GetClientRect, ITextDocument2::GetClientRect, controls.itextdocument2_getclientrect, tom/ITextDocument2::GetClientRect, tomClientCoord, tomIncludeInset, tomTransform
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
 - ITextDocument2.GetClientRect
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextDocument2::GetClientRect


## -description


Retrieves the client rectangle of the rich edit control.


## -parameters




### -param Type [in]

Type: <b>long</b>

The client rectangle retrieval options. It can be a combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="tomClientCoord"></a><a id="tomclientcoord"></a><a id="TOMCLIENTCOORD"></a><dl>
<dt><b>tomClientCoord</b></dt>
</dl>
</td>
<td width="60%">
Retrieve the rectangle in client coordinates. If this value isn't specified, the function retrieves screen coordinates.

</td>
</tr>
<tr>
<td width="40%"><a id="tomIncludeInset"></a><a id="tomincludeinset"></a><a id="TOMINCLUDEINSET"></a><dl>
<dt><b>tomIncludeInset</b></dt>
</dl>
</td>
<td width="60%">
Add left and top insets to the left and top coordinates of the client rectangle, and subtract right and bottom insets from the right and bottom coordinates. 

</td>
</tr>
<tr>
<td width="40%"><a id="tomTransform"></a><a id="tomtransform"></a><a id="TOMTRANSFORM"></a><dl>
<dt><b>tomTransform</b></dt>
</dl>
</td>
<td width="60%">
Use a world transform (XFORM) provided by the host application to transform the retrieved rectangle  coordinates.

</td>
</tr>
</table>
 


### -param pLeft [out]

Type: <b>long*</b>

The x-coordinate of the upper-left corner of the rectangle.


### -param pTop [out]

Type: <b>long*</b>

The y-coordinate of the upper-left corner of the rectangle.


### -param pRight [out]

Type: <b>long*</b>

The x-coordinate of the lower-right corner of the rectangle.


### -param pBottom [out]

Type: <b>long*</b>

The y-coordinate of the lower-right corner of the rectangle.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0b0a54d7-7606-41f6-b8be-6367d9180ef4">ITextDocument2</a>
 

 

