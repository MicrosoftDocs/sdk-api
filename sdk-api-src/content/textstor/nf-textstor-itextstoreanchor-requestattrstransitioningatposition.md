---
UID: NF:textstor.ITextStoreAnchor.RequestAttrsTransitioningAtPosition
title: ITextStoreAnchor::RequestAttrsTransitioningAtPosition
author: windows-driver-content
description: ITextStoreAnchor::RequestAttrsTransitioningAtPosition method
old-location: tsf\itextstoreanchor_requestattrstransitioningatposition.htm
old-project: TSF
ms.assetid: f0f43237-8c26-4e0c-8717-908884229b7b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RequestAttrsTransitioningAtPosition method, ITextStoreAnchor.RequestAttrsTransitioningAtPosition, ITextStoreAnchor::RequestAttrsTransitioningAtPosition, RequestAttrsTransitioningAtPosition, RequestAttrsTransitioningAtPosition method [Text Services Framework], RequestAttrsTransitioningAtPosition method [Text Services Framework],ITextStoreAnchor interface, TS_ATTR_FIND_WANT_END, TS_ATTR_FIND_WANT_VALUE, textstor/ITextStoreAnchor::RequestAttrsTransitioningAtPosition, tsf.itextstoreanchor_requestattrstransitioningatposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
-	ITextStoreAnchor.RequestAttrsTransitioningAtPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::RequestAttrsTransitioningAtPosition


## -description




## -parameters




### -param paPos [in]

Pointer to the anchor.


### -param cFilterAttrs [in]

Specifies the number of attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to verify.


### -param dwFlags [in]

Specifies attributes for the call to the <a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs</a> method. If this parameter is not set, the method returns the attributes that start at the specified anchor location. Other possible values for this parameter are the following.

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
Obtains the attributes that end at the specified anchor location.

</td>
</tr>
<tr>
<td width="40%"><a id="TS_ATTR_FIND_WANT_VALUE"></a><a id="ts_attr_find_want_value"></a><dl>
<dt><b>TS_ATTR_FIND_WANT_VALUE</b></dt>
</dl>
</td>
<td width="60%">
Obtains the value of the attribute in addition to the attribute. The attribute value is put into the <b>varValue</b> member of the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure during the <b>ITextStoreAnchor::RetrieveRequestedAttrs</b> method call.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>paPos</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



In the sentence, "This is <i>italic text</i>.", the italic attribute starts before the word <i>italic</i> and ends after the word <i>text</i>.

If the flag TS_ATTR_FIND_WANT_END is set in <i>dwFlags</i>, the method would return the italic attribute for the text "<i>italic</i> &lt;anchor&gt;normal", because there is an end transition at the anchor location.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">
        TS_ATTRID
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">
        TS_ATTRVAL
      </a>



<a href="https://msdn.microsoft.com/e99a44ba-c41a-4dd7-9475-dd37159081fd">
        TS_ATTR_* Constants
      </a>
 

 

