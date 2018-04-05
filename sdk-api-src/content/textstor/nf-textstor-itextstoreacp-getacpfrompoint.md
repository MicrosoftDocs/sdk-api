---
UID: NF:textstor.ITextStoreACP.GetACPFromPoint
title: ITextStoreACP::GetACPFromPoint method
author: windows-driver-content
description: The ITextStoreACP::GetACPFromPoint method converts a point in screen coordinates to an application character position.
old-location: tsf\itextstoreacp_getacpfrompoint.htm
old-project: TSF
ms.assetid: b6489391-a19e-405a-a129-f68054088860
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GXFPF_NEAREST, GXFPF_ROUND_NEAREST, GetACPFromPoint method [Text Services Framework], GetACPFromPoint method [Text Services Framework], ITextStoreACP interface, GetACPFromPoint,ITextStoreACP.GetACPFromPoint, ITextStoreACP, ITextStoreACP interface [Text Services Framework], GetACPFromPoint method, ITextStoreACP::GetACPFromPoint, _tsf_itextstoreacp_getacpfrompoint_ref, textstor/ITextStoreACP::GetACPFromPoint, tsf.itextstoreacp_getacpfrompoint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.GetACPFromPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::GetACPFromPoint method


## -description


The <b>ITextStoreACP::GetACPFromPoint</b> method converts a point in screen coordinates to an application character position.


## -parameters




### -param vcView [in]

Specifies the context view.


### -param ptScreen [in]

Pointer to the <b>POINT</b> structure with the screen coordinates of the point.


### -param dwFlags [in]

Specifies the character position to return based upon the screen coordinates of the point relative to a character bounding box. By default, the character position returned is the character bounding box containing the screen coordinates of the point. If the point is outside a character bounding box, the method returns <b>NULL</b> or <a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">TF_E_INVALIDPOINT</a>. Other bit flags for this parameter are as follows.

The bit flags can be combined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GXFPF_ROUND_NEAREST"></a><a id="gxfpf_round_nearest"></a><dl>
<dt><b>GXFPF_ROUND_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.

</td>
</tr>
<tr>
<td width="40%"><a id="GXFPF_NEAREST"></a><a id="gxfpf_nearest"></a><dl>
<dt><b>GXFPF_NEAREST</b></dt>
</dl>
</td>
<td width="60%">
If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.

</td>
</tr>
</table>
 


### -param pacp [out]

Receives the character position that corresponds to the screen coordinates of the point.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_INVALIDPOINT</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptScreen</i> parameter is not within the bounding box of any character.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLAYOUT</b></dt>
</dl>
</td>
<td width="60%">
The application has not calculated a text layout.

</td>
</tr>
</table>
 




## -remarks



<img alt="Point 1 is in character bounding box and point 2 is outside the character bounding box." border="border" src="images/ACPFig01.gif"/>
The point 1 screen coordinates cause the <i>pacp</i> parameter to be 0 by default or if the <i>dwFlags</i> parameter is set to <a href="https://msdn.microsoft.com/e69e5a4c-65e6-4d9b-8cb0-962524aa5d39">GXFPF_NEAREST</a> because the point 1 screen coordinates are inside the character bounding box of character position 0. If the <i>dwFlags</i> parameter is set to GXFPF_ROUND_NEAREST for point 1, the <i>pacp</i> parameter is 1 because the point 1 screen coordinates are closest to range position 1. Range position 1 is the starting range position of character position 1.

For the point 2 screen coordinates, the method returns <b>TF_E_INVALIDPOINT</b> by default or if the <i>dwFlags</i> parameter is set to <b>GXFPF_NEAREST</b> because the point 2 screen coordinates are outside a character bounding box. If the <i>dwFlags</i> parameter is set to <b>GXFPF_ROUND_NEAREST</b>, then the point 2 screen coordinates causes the <i>pacp</i> parameter to be 1, because the closest character position to the point 2 screen coordinates is character position 1.

<b>Point 1
      </b>

<ul>
<li>Default-- <i>pacp = 0</i> --The screen coordinates point is inside the character bounding box of Character Position 0.</li>
<li><b>GXFPF_ROUND_NEAREST</b> -- <i>pacp = 1</i> --The screen coordinates of the point is closest to Range Position 1 which is the starting range position of Character Position 1.</li>
<li><b>GXFPF_NEAREST</b> -- <i>pacp = 0</i> --The default behavior occurs because the point is within the character bounding box of Character Position 0.</li>
</ul>
<b>Point 2</b>

<ul>
<li>Default-- <i>hr = TF_E_INVALIDPOINT</i> --The screen coordinates of the point is outside a character bounding box.</li>
<li>GXPF_ROUND_NEAREST-- <i>hr = TF_E_INVALIDPOINT</i> --The default behavior occurs because the screen coordinates of the point are outside a character bounding box.</li>
<li>GXPF_NEAREST-- <i>pacp = 1</i> --The closest character position to the screen coordinates of the point is Character Position 1.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/e69e5a4c-65e6-4d9b-8cb0-962524aa5d39">GXFPF_* Constants
      </a>



<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/f8091e79-33af-49d5-b3c8-d30952c62010">
        ITfContextOwner::GetACPFromPoint
      </a>



<a href="https://msdn.microsoft.com/543761fe-420e-4821-a69f-abc6c853677e">
        ITfContextView::GetRangeFromPoint
      </a>



<a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">
        Manager Return Values
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

