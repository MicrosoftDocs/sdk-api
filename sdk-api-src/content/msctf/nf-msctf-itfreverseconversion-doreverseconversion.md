---
UID: NF:msctf.ITfReverseConversion.DoReverseConversion
title: ITfReverseConversion::DoReverseConversion
author: windows-driver-content
description: Performs a reverse conversion of the specified string.
old-location: tsf\itfreverseconversion__doreverseconversion.htm
old-project: TSF
ms.assetid: a2312cd4-316a-42a6-85a5-e5ef819faa79
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: DoReverseConversion, DoReverseConversion method [Text Services Framework], DoReverseConversion method [Text Services Framework],ITfReverseConversion interface, ITfReverseConversion interface [Text Services Framework],DoReverseConversion method, ITfReverseConversion.DoReverseConversion, ITfReverseConversion::DoReverseConversion, msctf/ITfReverseConversion::DoReverseConversion, tsf.itfreverseconversion__doreverseconversion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfReverseConversion.DoReverseConversion
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfReverseConversion::DoReverseConversion


## -description


<p class="CCE_Message">[<b>DoReverseConversion</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For internal use only.]

Performs a reverse conversion of the specified string. 


## -parameters




### -param lpstr [in]

The string to convert. 


### -param ppList [out]

 The result of the conversion: a list of the key strokes required to create the string specied by <i>lpstr</i>.  


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
The conversion result is stored in <i>ppList</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_FALSE</dt>
</dl>
</td>
<td width="60%">
The conversion result, <i>ppList</i>, contains no entries.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_FAIL</dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



A reverse conversion provides the keystroke sequences required to create the specified string.




## -see-also




<a href="https://msdn.microsoft.com/ca2e036a-d0f8-4372-872a-388217050d15">ITfReverseConversion</a>
 

 

