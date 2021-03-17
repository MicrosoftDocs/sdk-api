---
UID: NF:rend.ITDirectoryObjectUser.get_IPPhonePrimary
title: ITDirectoryObjectUser::get_IPPhonePrimary (rend.h)
description: The get_IPPhonePrimary method gets the name of a computer that is the primary IP phone for the user.
helpviewer_keywords: ["ITDirectoryObjectUser interface [TAPI 2.2]","get_IPPhonePrimary method","ITDirectoryObjectUser.get_IPPhonePrimary","ITDirectoryObjectUser::get_IPPhonePrimary","_tapi3_itdirectoryobjectuser_get_ipphoneprimary","get_IPPhonePrimary","get_IPPhonePrimary method [TAPI 2.2]","get_IPPhonePrimary method [TAPI 2.2]","ITDirectoryObjectUser interface","rend/ITDirectoryObjectUser::get_IPPhonePrimary","tapi3.itdirectoryobjectuser_get_ipphoneprimary"]
old-location: tapi3\itdirectoryobjectuser_get_ipphoneprimary.htm
tech.root: tapi3
ms.assetid: 43bb9ce5-28ff-4a6f-a55c-a84633e22dfe
ms.date: 12/05/2018
ms.keywords: ITDirectoryObjectUser interface [TAPI 2.2],get_IPPhonePrimary method, ITDirectoryObjectUser.get_IPPhonePrimary, ITDirectoryObjectUser::get_IPPhonePrimary, _tapi3_itdirectoryobjectuser_get_ipphoneprimary, get_IPPhonePrimary, get_IPPhonePrimary method [TAPI 2.2], get_IPPhonePrimary method [TAPI 2.2],ITDirectoryObjectUser interface, rend/ITDirectoryObjectUser::get_IPPhonePrimary, tapi3.itdirectoryobjectuser_get_ipphoneprimary
req.header: rend.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Rend.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITDirectoryObjectUser::get_IPPhonePrimary
 - rend/ITDirectoryObjectUser::get_IPPhonePrimary
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObjectUser.get_IPPhonePrimary
---

# ITDirectoryObjectUser::get_IPPhonePrimary


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_IPPhonePrimary</b> method gets the name of a computer that is the primary IP phone for the user.

## -parameters

### -param ppName [out]

Pointer to the <b>BSTR</b> representation of the user's IP primary phone.

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
Invalid pointer.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobjectuser">ITDirectoryObjectUser</a>



<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobjectuser-put_ipphoneprimary">ITDirectoryObjectUser::put_IPPhonePrimary</a>