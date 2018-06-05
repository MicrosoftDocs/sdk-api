---
UID: NF:ctffunc.IEnumTfLatticeElements.Next
title: IEnumTfLatticeElements::Next
author: windows-sdk-content
description: IEnumTfLatticeElements::Next method
old-location: tsf\ienumtflatticeelements_next.htm
old-project: TSF
ms.assetid: 066493c9-6597-43f4-9f65-51578af00a9b
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: IEnumTfLatticeElements interface [Text Services Framework],Next method, IEnumTfLatticeElements.Next, IEnumTfLatticeElements::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumTfLatticeElements interface, _tsf_ienumtflatticeelements_next_ref, ctffunc/IEnumTfLatticeElements::Next, tsf.ienumtflatticeelements_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sptip.dll
api_name:
-	IEnumTfLatticeElements.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Sptip.dll
req.irql: 
---

# IEnumTfLatticeElements::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param rgsElements [out]

Pointer to an array of <a href="https://msdn.microsoft.com/55cc631f-c9ab-4ca8-ab5b-43e8a2e88fc9">TF_LMLATTELEMENT</a> structures that receives the requested data. This array must be at least <i>ulCount</i> elements in size.

The caller must free the <b>bstrText</b> member of every structure obtained using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements actually obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rgsElements</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">IEnumTfLatticeElements</a>



<a href="https://msdn.microsoft.com/55cc631f-c9ab-4ca8-ab5b-43e8a2e88fc9">TF_LMLATTELEMENT
      </a>
 

 

