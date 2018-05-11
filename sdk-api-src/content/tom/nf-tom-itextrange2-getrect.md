---
UID: NF:tom.ITextRange2.GetRect
title: ITextRange2::GetRect
author: windows-driver-content
description: Retrieves a rectangle of the specified type for the current range.
old-location: controls\itextrange2_getrect.htm
old-project: Controls
ms.assetid: 14f0faab-ff37-4f86-a4ba-b6c207d7ddf0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetRect, GetRect method [Windows Controls], GetRect method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetRect method, ITextRange2.GetRect, ITextRange2::GetRect, controls.itextrange2_getrect, tom/ITextRange2::GetRect, tomAllowOffClient, tomClientCoord, tomObjectArg, tomTransform
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
-	ITextRange2.GetRect
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRange2::GetRect


## -description


Retrieves a rectangle of the specified type for the current range.


## -parameters




### -param Type [in]

Type: <b>long</b>

The type of rectangle to return. This parameter can include one value from each of the following tables. 

<a id="tomAllowOffClient"></a>
<a id="tomallowoffclient"></a>
<a id="TOMALLOWOFFCLIENT"></a>


#### tomAllowOffClient

<a id="tomClientCoord"></a>
<a id="tomclientcoord"></a>
<a id="TOMCLIENTCOORD"></a>


#### tomClientCoord

<a id="tomObjectArg"></a>
<a id="tomobjectarg"></a>
<a id="TOMOBJECTARG"></a>


#### tomObjectArg

<a id="tomTransform"></a>
<a id="tomtransform"></a>
<a id="TOMTRANSFORM"></a>


#### tomTransform

Use one of these values to indicate the vertical position: 
						<table class="clsStd">
<tr>
<td>TA_TOP</td>
<td>Top edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_BASELINE</td>
<td>Base line of the text.</td>
</tr>
<tr>
<td>TA_BOTTOM</td>
<td>Bottom edge of the bounding rectangle.</td>
</tr>
</table>
 



Use one of these values to indicate the horizontal position: 
						<table class="clsStd">
<tr>
<td>TA_LEFT</td>
<td>Left edge of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_CENTER</td>
<td>Center of the bounding rectangle.</td>
</tr>
<tr>
<td>TA_RIGHT</td>
<td>Right edge of the bounding rectangle.</td>
</tr>
</table>
 




### -param pLeft [out]

Type: <b>long*</b>

The left rectangle coordinate.


### -param pTop [out]

Type: <b>long*</b>

The top rectangle coordinate.


### -param pRight [out]

Type: <b>long*</b>

The right rectangle coordinate.


### -param pBottom [out]

Type: <b>long*</b>

The bottom rectangle coordinate.


### -param pHit [out]

Type: <b>long*</b>

The hit-test value for the range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>
 

 

