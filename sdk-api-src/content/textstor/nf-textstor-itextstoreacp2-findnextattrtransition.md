---
UID: NF:textstor.ITextStoreACP2.FindNextAttrTransition
title: ITextStoreACP2::FindNextAttrTransition method
author: windows-driver-content
description: Determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.
old-location: tsf\itextstoreacp2_findnextattrtransition.htm
old-project: TSF
ms.assetid: 8ccad786-64e0-423c-8b8e-c853123828e5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: FindNextAttrTransition method [Text Services Framework], FindNextAttrTransition method [Text Services Framework], ITextStoreACP2 interface, FindNextAttrTransition,ITextStoreACP2.FindNextAttrTransition, ITextStoreACP2, ITextStoreACP2 interface [Text Services Framework], FindNextAttrTransition method, ITextStoreACP2::FindNextAttrTransition, TS_ATTR_FIND_BACKWARDS, TS_ATTR_FIND_WANT_OFFSET, textstor/ITextStoreACP2::FindNextAttrTransition, tsf.itextstoreacp2_findnextattrtransition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
-	ITextStoreACP2.FindNextAttrTransition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP2::FindNextAttrTransition method


## -description


Determines the character position where a transition occurs in an attribute value. The specified attribute to check is application-dependent.


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



<div class="alert"><b>Note</b>  If an application does not implement <b>FindNextAttrTransition</b>, <a href="https://msdn.microsoft.com/201c518b-f06f-4c4f-aa56-f8d21f477814">ITfReadOnlyProperty::EnumRanges</a> fails with <b>E_FAIL</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">
        TS_ATTRID
      </a>



<a href="https://msdn.microsoft.com/e99a44ba-c41a-4dd7-9475-dd37159081fd">TS_ATTR_* Constants
      </a>
 

 

