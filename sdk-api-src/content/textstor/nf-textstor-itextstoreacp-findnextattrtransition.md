---
UID: NF:textstor.ITextStoreACP.FindNextAttrTransition
title: ITextStoreACP::FindNextAttrTransition method
author: windows-driver-content
description: The ITextStoreACP::FindNextAttrTransition method determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.
old-location: tsf\itextstoreacp_findnextattrtransition.htm
old-project: TSF
ms.assetid: f5917958-150e-48a5-9d0d-67240a88c232
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: FindNextAttrTransition method [Text Services Framework], FindNextAttrTransition method [Text Services Framework], ITextStoreACP interface, FindNextAttrTransition,ITextStoreACP.FindNextAttrTransition, ITextStoreACP, ITextStoreACP interface [Text Services Framework], FindNextAttrTransition method, ITextStoreACP::FindNextAttrTransition, TS_ATTR_FIND_BACKWARDS, TS_ATTR_FIND_WANT_OFFSET, _tsf_itextstoreacp_findnextattrtransition_ref, textstor/ITextStoreACP::FindNextAttrTransition, tsf.itextstoreacp_findnextattrtransition
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
-	ITextStoreACP.FindNextAttrTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::FindNextAttrTransition method


## -description


The <b>ITextStoreACP::FindNextAttrTransition</b> method determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.


## -parameters




### -param acpStart [in]

Specifies the character position to start the search for an attribute transition.


### -param acpHalt [in]

Specifies the character position to end the search for an attribute transition.


### -param cFilterAttrs [in]

Specifies the number of attributes to check.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to check.


### -param dwFlags [in]

Specifies the direction to search for an attribute transition. By default, the method searches forward.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_BACKWARDS"></a><a id="ts_attr_find_backwards"></a><dl>
<dt><b>TS_ATTR_FIND_BACKWARDS</b></dt>
</dl>
</td>
<td width="60%">
The method searches backward.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_OFFSET"></a><a id="ts_attr_find_want_offset"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_OFFSET</b></dt>
</dl>
</td>
<td width="60%">
The <i>plFoundOffset</i> parameter receives the character offset of the attribute transition from <i>acpStart</i>.

</td>
</tr>
</table>
 


### -param pacpNext [out]

Receives the next character position to check for an attribute transition.


### -param pfFound [out]

Receives a Boolean value of <b>TRUE</b> if an attribute transition was found, otherwise <b>FALSE</b> is returned.


### -param plFoundOffset [out]

Receives the character position of the attribute transition (not ACP positions). If TS_ATTR_FIND_WANT_OFFSET flag is set in <i>dwFlags</i>, receives the character offset of the attribute transition from <i>acpStart</i>.


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
<dt><b>TS_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The character positions specified are beyond the text in the document.

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  If an application does not implement <b>ITextStoreACP::FindNextAttrTransition</b>, <a href="https://msdn.microsoft.com/201c518b-f06f-4c4f-aa56-f8d21f477814">ITfReadOnlyProperty::EnumRanges</a> fails with E_FAIL.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">
        TS_ATTRID
      </a>



<a href="https://msdn.microsoft.com/e99a44ba-c41a-4dd7-9475-dd37159081fd">TS_ATTR_* Constants
      </a>
 

 

