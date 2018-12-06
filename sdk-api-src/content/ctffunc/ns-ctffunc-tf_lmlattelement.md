---
UID: NS:ctffunc.TF_LMLATTELEMENT
title: TF_LMLATTELEMENT
author: windows-sdk-content
description: The TF_LMLATTELEMENT structure contains information about a lattice element. A lattice element is used in speech recognition. This structure is used with the IEnumTfLatticeElements::Next method.
old-location: tsf\tf_lmlattelement.htm
tech.root: TSF
ms.assetid: 55cc631f-c9ab-4ca8-ab5b-43e8a2e88fc9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TF_LMLATTELEMENT, TF_LMLATTELEMENT structure [Text Services Framework], _tsf_tf_lmlattelement_ref, ctffunc/TF_LMLATTELEMENT, tsf.tf_lmlattelement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ctffunc.h
api_name:
 - TF_LMLATTELEMENT
product: Windows
targetos: Windows
req.typenames: TF_LMLATTELEMENT
req.redist: TSF 1.0 on Windows 2000 Professional
---

# TF_LMLATTELEMENT structure


## -description



The <b>TF_LMLATTELEMENT</b> structure contains information about a lattice element. A lattice element is used in speech recognition. This structure is used with the <a href="https://msdn.microsoft.com/066493c9-6597-43f4-9f65-51578af00a9b">IEnumTfLatticeElements::Next</a> method.




## -struct-fields




### -field dwFrameStart

Contains the starting offset, in 100-nanosecond units, of the element relative to the start of the phrase.


### -field dwFrameLen

Contains the length, in 100-nanosecond units, of the element.


### -field dwFlags

Not currently used.


### -field iCost

Specifies the actual confidence for this element. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>SP_LOW_CONFIDENCE</td>
<td>The speech engine has low confidence in the element.</td>
</tr>
<tr>
<td>SP_NORMAL_CONFIDENCE</td>
<td>The speech engine has normal confidence in the element.</td>
</tr>
<tr>
<td>SP_HIGH_CONFIDENCE</td>
<td>The speech engine has high confidence in the element.</td>
</tr>
</table>
 


### -field bstrText

Contains the display text for the element. If the spoken word is "two", the display text will be "2". The caller must free this string using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


## -see-also




<a href="https://msdn.microsoft.com/066493c9-6597-43f4-9f65-51578af00a9b">IEnumTfLatticeElements::Next
      </a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

