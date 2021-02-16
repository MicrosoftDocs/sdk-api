---
UID: NF:rend.ITDirectoryObject.get_DialableAddrs
title: ITDirectoryObject::get_DialableAddrs (rend.h)
description: The get_DialableAddrs method gets all dialable addresses of a given type from the directory. This method performs the same function as EnumerateDialableAddrs but is used by scripting languages such as Visual Basic.
helpviewer_keywords: ["ITDirectoryObject interface [TAPI 2.2]","get_DialableAddrs method","ITDirectoryObject.get_DialableAddrs","ITDirectoryObject::get_DialableAddrs","_tapi3_itdirectoryobject_get_dialableaddrs","get_DialableAddrs","get_DialableAddrs method [TAPI 2.2]","get_DialableAddrs method [TAPI 2.2]","ITDirectoryObject interface","rend/ITDirectoryObject::get_DialableAddrs","tapi3.itdirectoryobject_get_dialableaddrs"]
old-location: tapi3\itdirectoryobject_get_dialableaddrs.htm
tech.root: tapi3
ms.assetid: b72e9c49-4d5a-432a-b21b-ec444912ea61
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],get_DialableAddrs method, ITDirectoryObject.get_DialableAddrs, ITDirectoryObject::get_DialableAddrs, _tapi3_itdirectoryobject_get_dialableaddrs, get_DialableAddrs, get_DialableAddrs method [TAPI 2.2], get_DialableAddrs method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::get_DialableAddrs, tapi3.itdirectoryobject_get_dialableaddrs
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
 - ITDirectoryObject::get_DialableAddrs
 - rend/ITDirectoryObject::get_DialableAddrs
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
 - ITDirectoryObject.get_DialableAddrs
---

# ITDirectoryObject::get_DialableAddrs


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DialableAddrs</b> method gets all dialable addresses of a given type from the directory. This method performs the same function as 
<a href="/windows/desktop/api/rend/nf-rend-itdirectoryobject-enumeratedialableaddrs">EnumerateDialableAddrs</a> but is used by scripting languages such as Visual Basic.

## -parameters

### -param dwAddressType [in]

Indicator of address type.

### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of <b>BSTR</b> strings, each containing a dialable address.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface returned by <b>ITDirectoryObject::get_DialableAddrs</b>. The application must call <b>Release</b> on the 
<b>ITAddress</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a>