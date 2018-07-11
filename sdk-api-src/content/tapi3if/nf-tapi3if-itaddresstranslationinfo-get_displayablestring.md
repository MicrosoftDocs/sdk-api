---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DisplayableString
title: ITAddressTranslationInfo::get_DisplayableString
author: windows-sdk-content
description: The get_DisplayableString method gets a string that contains a displayable version of the dialable number.
old-location: tapi3\itaddresstranslationinfo_get_displayablestring.htm
old-project: tapi
ms.assetid: c88474ee-5a7e-4966-8dc2-5f839069b2d2
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DisplayableString method, ITAddressTranslationInfo.get_DisplayableString, ITAddressTranslationInfo::get_DisplayableString, _tapi3_itaddresstranslationinfo_get_displayablestring, get_DisplayableString, get_DisplayableString method [TAPI 2.2], get_DisplayableString method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_displayablestring, tapi3if/ITAddressTranslationInfo::get_DisplayableString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslationInfo.get_DisplayableString
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAddressTranslationInfo::get_DisplayableString


## -description


The 
<b>get_DisplayableString</b> method gets a string that contains a displayable version of the dialable number.


## -parameters




### -param ppDisplayableString [out]

Pointer to <b>BSTR</b> containing representation of displayable string.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDisplayableString</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppDisplayableString</i> parameter.
			

Corresponds to the <b>dwDisplayableStringSize</b> and <b>dwDisplayableStringOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>
 

 

