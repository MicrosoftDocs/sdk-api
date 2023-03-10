---
UID: NF:rend.IEnumDirectoryObject.Next
title: IEnumDirectoryObject::Next (rend.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. (IEnumDirectoryObject.Next)
helpviewer_keywords: ["IEnumDirectoryObject interface [TAPI 2.2]","Next method","IEnumDirectoryObject.Next","IEnumDirectoryObject::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumDirectoryObject interface","_tapi3_ienumdirectoryobject_next","rend/IEnumDirectoryObject::Next","tapi3.ienumdirectoryobject_next"]
old-location: tapi3\ienumdirectoryobject_next.htm
tech.root: tapi3
ms.assetid: 034a704a-f5c7-46bf-a8fa-9bb6298dd4d2
ms.date: 12/05/2018
ms.keywords: IEnumDirectoryObject interface [TAPI 2.2],Next method, IEnumDirectoryObject.Next, IEnumDirectoryObject::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumDirectoryObject interface, _tapi3_ienumdirectoryobject_next, rend/IEnumDirectoryObject::Next, tapi3.ienumdirectoryobject_next
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
 - IEnumDirectoryObject::Next
 - rend/IEnumDirectoryObject::Next
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
 - IEnumDirectoryObject.Next
---

# IEnumDirectoryObject::Next


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param pVal [out]

Pointer to the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> interface.

### -param pcFetched [out]

Pointer to the number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVal</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> interface returned by <b>IEnumDirectoryObject::Next</b>. The application must call <b>Release</b> on the 
<b>ITDirectoryObject</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-ienumdirectoryobject">IEnumDirectoryObject</a>
