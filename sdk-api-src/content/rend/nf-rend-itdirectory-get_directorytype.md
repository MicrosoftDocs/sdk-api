---
UID: NF:rend.ITDirectory.get_DirectoryType
title: ITDirectory::get_DirectoryType (rend.h)
description: The get_DirectoryType method gets DIRECTORY_TYPE indicator of the type of the directory.
helpviewer_keywords: ["ITDirectory interface [TAPI 2.2]","get_DirectoryType method","ITDirectory.get_DirectoryType","ITDirectory::get_DirectoryType","_tapi3_itdirectory_get_directorytype","get_DirectoryType","get_DirectoryType method [TAPI 2.2]","get_DirectoryType method [TAPI 2.2]","ITDirectory interface","rend/ITDirectory::get_DirectoryType","tapi3.itdirectory_get_directorytype"]
old-location: tapi3\itdirectory_get_directorytype.htm
tech.root: tapi3
ms.assetid: 3f0ca4c2-4ba9-4a6e-877b-36486086368f
ms.date: 12/05/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DirectoryType method, ITDirectory.get_DirectoryType, ITDirectory::get_DirectoryType, _tapi3_itdirectory_get_directorytype, get_DirectoryType, get_DirectoryType method [TAPI 2.2], get_DirectoryType method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DirectoryType, tapi3.itdirectory_get_directorytype
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
 - ITDirectory::get_DirectoryType
 - rend/ITDirectory::get_DirectoryType
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
 - ITDirectory.get_DirectoryType
---

# ITDirectory::get_DirectoryType


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DirectoryType</b> method gets 
<a href="/windows/desktop/api/rend/ne-rend-directory_type">DIRECTORY_TYPE</a> indicator of the type of the directory.

## -parameters

### -param pDirectoryType [out]

Pointer to type of the directory.

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
The <i>pDirectoryType</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/rend/ne-rend-directory_type">DIRECTORY_TYPE</a>



<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>