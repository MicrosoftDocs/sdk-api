---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DialableString
title: ITAddressTranslationInfo::get_DialableString
author: windows-sdk-content
description: The get_DialableString method gets a string that contains a dialable number. Typically, this number is then used as the pDestAddress argument in ITAddress::CreateCall.
old-location: tapi3\itaddresstranslationinfo_get_dialablestring.htm
tech.root: tapi
ms.assetid: 76177de9-eab2-4a86-ac25-29b78606b854
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DialableString method, ITAddressTranslationInfo.get_DialableString, ITAddressTranslationInfo::get_DialableString, _tapi3_itaddresstranslationinfo_get_dialablestring, get_DialableString, get_DialableString method [TAPI 2.2], get_DialableString method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_dialablestring, tapi3if/ITAddressTranslationInfo::get_DialableString
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslationInfo.get_DialableString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAddressTranslationInfo::get_DialableString


## -description


The 
<b>get_DialableString</b> method gets a string that contains a dialable number. Typically, this number is then used as the <i>pDestAddress</i> argument in 
<a href="https://msdn.microsoft.com/1b5a755c-fdaf-42ca-9747-9b34efbd0ac3">ITAddress::CreateCall</a>.


## -parameters




### -param ppDialableString [out]

Pointer to <b>BSTR</b> containing representation of dialable string.


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
The <i>ppDialableString</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> to free the memory allocated for the <i>ppDialableString</i> parameter.
			

Corresponds to the <b>dwDialableStringSize</b> and <b>dwDialableStringOffset</b> members of TAPI 2's 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>
 

 

