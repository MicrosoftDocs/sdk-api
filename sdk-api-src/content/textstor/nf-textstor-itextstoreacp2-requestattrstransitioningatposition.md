---
UID: NF:textstor.ITextStoreACP2.RequestAttrsTransitioningAtPosition
title: ITextStoreACP2::RequestAttrsTransitioningAtPosition (textstor.h)
description: Gets text attributes transitioning at the specified character position.
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","RequestAttrsTransitioningAtPosition method","ITextStoreACP2.RequestAttrsTransitioningAtPosition","ITextStoreACP2::RequestAttrsTransitioningAtPosition","RequestAttrsTransitioningAtPosition","RequestAttrsTransitioningAtPosition method [Text Services Framework]","RequestAttrsTransitioningAtPosition method [Text Services Framework]","ITextStoreACP2 interface","TS_ATTR_FIND_WANT_END","TS_ATTR_FIND_WANT_VALUE","textstor/ITextStoreACP2::RequestAttrsTransitioningAtPosition","tsf.itextstoreacp2_requestattrstransitioningatposition"]
old-location: tsf\itextstoreacp2_requestattrstransitioningatposition.htm
tech.root: TSF
ms.assetid: ff1cda58-f02d-4c39-aed5-ebacbef20780
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RequestAttrsTransitioningAtPosition method, ITextStoreACP2.RequestAttrsTransitioningAtPosition, ITextStoreACP2::RequestAttrsTransitioningAtPosition, RequestAttrsTransitioningAtPosition, RequestAttrsTransitioningAtPosition method [Text Services Framework], RequestAttrsTransitioningAtPosition method [Text Services Framework],ITextStoreACP2 interface, TS_ATTR_FIND_WANT_END, TS_ATTR_FIND_WANT_VALUE, textstor/ITextStoreACP2::RequestAttrsTransitioningAtPosition, tsf.itextstoreacp2_requestattrstransitioningatposition
f1_keywords:
- textstor/ITextStoreACP2.RequestAttrsTransitioningAtPosition
dev_langs:
- c++
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- msctf.dll
api_name:
- ITextStoreACP2.RequestAttrsTransitioningAtPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextStoreACP2::RequestAttrsTransitioningAtPosition


## -description


Gets text attributes transitioning at the specified character position.


## -parameters




### -param acpPos [in]

Specifies the application character position in the document.


### -param cFilterAttrs [in]

Specifies the number of attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to verify.


### -param dwFlags [in]

Specifies attributes for the call to the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-retrieverequestedattrs">RetrieveRequestedAttrs</a> method. If this parameter is not set, the method returns the attributes that start at the specified position. Other possible values for this parameter are the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_END"></a><a id="ts_attr_find_want_end"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_END</b></dt>
</dl>
</td>
<td width="60%">
Obtains the attributes that end at the specified application character position.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_VALUE"></a><a id="ts_attr_find_want_value"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Obtains the value of the attribute in addition to the attribute. The attribute value is put into the <b>varValue</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a> structure during the <a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-retrieverequestedattrs">RetrieveRequestedAttrs</a> method call.

</td>
</tr>
</table>
 


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
</table>
 




## -remarks



In the sentence, "This is <i>italic text</i>.", the italic attribute starts before the word <i>italic</i> and ends after the word <i>text</i>.

If the flag TS_ATTR_FIND_WANT_END is set in <i>dwFlags</i>, the method would return the italic attribute for the text "<i>italic</i> &lt;anchor&gt;normal", because there is an end transition at the anchor location.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-retrieverequestedattrs">RetrieveRequestedAttrs</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/ts-attrid">TS_ATTRID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a>



<a href="https://docs.microsoft.com/windows/desktop/TSF/ts-attr--constants">TS_ATTR_* Constants
      </a>
 

 

