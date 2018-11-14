---
UID: NF:tapi3if.ITAddressTranslationInfo.get_TranslationResults
title: ITAddressTranslationInfo::get_TranslationResults
author: windows-sdk-content
description: The get_TranslationResults method gets the results of a translation operation.
old-location: tapi3\itaddresstranslationinfo_get_translationresults.htm
tech.root: tapi
ms.assetid: ca6ac2c9-612d-4294-ab49-7c0278519a24
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_TranslationResults method, ITAddressTranslationInfo.get_TranslationResults, ITAddressTranslationInfo::get_TranslationResults, _tapi3_itaddresstranslationinfo_get_translationresults, get_TranslationResults, get_TranslationResults method [TAPI 2.2], get_TranslationResults method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_translationresults, tapi3if/ITAddressTranslationInfo::get_TranslationResults
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
 - ITAddressTranslationInfo.get_TranslationResults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITAddressTranslationInfo.get_TranslationResults
: 
---

# ITAddressTranslationInfo::get_TranslationResults


## -description


The 
<b>get_TranslationResults</b> method gets the results of a translation operation.


## -parameters




### -param plResults [out]

Indicates the information derived from the translation process, which may assist the application in presenting user-interface elements. This value uses one of the 
<a href="https://msdn.microsoft.com/7b834c57-d862-4fe6-828c-9e8fa20f3ec7">LINETRANSLATERESULT_ Constants</a>.


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
The <i>plResults</i> parameter is not a valid pointer.

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



Corresponds to the <b>dwTranslateResults</b> member of TAPI 2's 
<a href="https://msdn.microsoft.com/bcf094ad-8098-4e45-9131-25dbdb7e4093">LINETRANSLATEOUTPUT</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/b59454a0-315f-4160-b969-d930c13bb4de">ITAddressTranslationInfo</a>
 

 

