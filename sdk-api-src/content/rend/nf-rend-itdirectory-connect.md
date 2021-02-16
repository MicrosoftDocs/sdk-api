---
UID: NF:rend.ITDirectory.Connect
title: ITDirectory::Connect (rend.h)
description: The Connect method establishes a connection to the directory server.
helpviewer_keywords: ["Connect","Connect method [TAPI 2.2]","Connect method [TAPI 2.2]","ITDirectory interface","ITDirectory interface [TAPI 2.2]","Connect method","ITDirectory.Connect","ITDirectory::Connect","_tapi3_itdirectory_connect","rend/ITDirectory::Connect","tapi3.itdirectory_connect"]
old-location: tapi3\itdirectory_connect.htm
tech.root: tapi3
ms.assetid: b781008b-430a-444e-a700-8cde09e721b4
ms.date: 12/05/2018
ms.keywords: Connect, Connect method [TAPI 2.2], Connect method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],Connect method, ITDirectory.Connect, ITDirectory::Connect, _tapi3_itdirectory_connect, rend/ITDirectory::Connect, tapi3.itdirectory_connect
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
 - ITDirectory::Connect
 - rend/ITDirectory::Connect
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
 - ITDirectory.Connect
---

# ITDirectory::Connect


## -description

<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>Connect</b> method establishes a connection to the directory server.

## -parameters

### -param fSecure [in]

Boolean indicator of whether to use SSL connection.

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
<dt><b>RND_ALREADY_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
A successful connection has already been made.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RND_NULL_SERVER_NAME</b></dt>
</dl>
</td>
<td width="60%">
The server name is <b>NULL</b>, probably because 
<a href="/windows/desktop/Tapi/itconferenceblob-init">ITConferenceBlob::Init</a> has not been run or did not succeed.

</td>
</tr>
</table>

## -remarks

The 
<b>Connect</b> method must be successfully called before any other function except 
<a href="/windows/desktop/api/rend/nf-rend-itdirectory-get_directorytype">get_DirectoryType</a>.

## -see-also

<a href="/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a>