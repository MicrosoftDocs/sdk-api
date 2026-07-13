---
UID: NF:rend.IEnumDirectoryObject.Skip
title: IEnumDirectoryObject::Skip (rend.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence. (IEnumDirectoryObject.Skip)
helpviewer_keywords: ["IEnumDirectoryObject interface [TAPI 2.2]","Skip method","IEnumDirectoryObject.Skip","IEnumDirectoryObject::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumDirectoryObject interface","_tapi3_ienumdirectoryobject_skip","rend/IEnumDirectoryObject::Skip","tapi3.ienumdirectoryobject_skip"]
old-location: tapi3\ienumdirectoryobject_skip.htm
tech.root: tapi3
ms.assetid: e14e71f1-5151-4562-bfbf-1370f65cb23a
ms.date: 12/05/2018
ms.keywords: IEnumDirectoryObject interface [TAPI 2.2],Skip method, IEnumDirectoryObject.Skip, IEnumDirectoryObject::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumDirectoryObject interface, _tapi3_ienumdirectoryobject_skip, rend/IEnumDirectoryObject::Skip, tapi3.ienumdirectoryobject_skip
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
 - IEnumDirectoryObject::Skip
 - rend/IEnumDirectoryObject::Skip
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
 - IEnumDirectoryObject.Skip
---

# IEnumDirectoryObject::Skip


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

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
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-ienumdirectoryobject">IEnumDirectoryObject</a>
