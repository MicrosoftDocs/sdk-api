---
UID: NF:tapi3if.ITAddressTranslationInfo.get_TranslationResults
title: ITAddressTranslationInfo::get_TranslationResults (tapi3if.h)
description: The get_TranslationResults method gets the results of a translation operation.
helpviewer_keywords: ["ITAddressTranslationInfo interface [TAPI 2.2]","get_TranslationResults method","ITAddressTranslationInfo.get_TranslationResults","ITAddressTranslationInfo::get_TranslationResults","_tapi3_itaddresstranslationinfo_get_translationresults","get_TranslationResults","get_TranslationResults method [TAPI 2.2]","get_TranslationResults method [TAPI 2.2]","ITAddressTranslationInfo interface","tapi3.itaddresstranslationinfo_get_translationresults","tapi3if/ITAddressTranslationInfo::get_TranslationResults"]
old-location: tapi3\itaddresstranslationinfo_get_translationresults.htm
tech.root: tapi3
ms.assetid: ca6ac2c9-612d-4294-ab49-7c0278519a24
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_TranslationResults method, ITAddressTranslationInfo.get_TranslationResults, ITAddressTranslationInfo::get_TranslationResults, _tapi3_itaddresstranslationinfo_get_translationresults, get_TranslationResults, get_TranslationResults method [TAPI 2.2], get_TranslationResults method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_translationresults, tapi3if/ITAddressTranslationInfo::get_TranslationResults
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAddressTranslationInfo::get_TranslationResults
 - tapi3if/ITAddressTranslationInfo::get_TranslationResults
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAddressTranslationInfo.get_TranslationResults
---

# ITAddressTranslationInfo::get_TranslationResults


## -description

The 
<b>get_TranslationResults</b> method gets the results of a translation operation.

## -parameters

### -param plResults [out]

Indicates the information derived from the translation process, which may assist the application in presenting user-interface elements. This value uses one of the 
<a href="/windows/desktop/Tapi/linetranslateresult--constants">LINETRANSLATERESULT_ Constants</a>.

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
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>