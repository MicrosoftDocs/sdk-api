---
UID: NS:npapi._NOTIFYADD
title: "_NOTIFYADD"
author: windows-driver-content
description: The NOTIFYADD structure contains the details of a network connect operation. It is used by the AddConnectNotify function.
old-location: security\notifyadd.htm
old-project: SecAuthN
ms.assetid: 23698bd9-12f6-4c1f-b833-bd5fddeba048
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*LPNOTIFYADD, CONNECT_INTERACTIVE, CONNECT_PROMPT, CONNECT_TEMPORARY, CONNECT_UPDATE_PROFILE, CONNECT_UPDATE_RECENT, LPNOTIFYADD, LPNOTIFYADD structure pointer [Security], NOTIFYADD, NOTIFYADD structure [Security], _NOTIFYADD, _mnp_notifyadd, npapi/LPNOTIFYADD, npapi/NOTIFYADD, security.notifyadd"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NOTIFYADD, *LPNOTIFYADD
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Npapi.h
api_name:
-	NOTIFYADD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _NOTIFYADD structure


## -description


The <b>NOTIFYADD</b> structure contains the details of a network connect operation. It is used by the 
<a href="https://msdn.microsoft.com/a061b088-81ca-4276-a0d6-9f1d1282a039">AddConnectNotify</a> function.


## -struct-fields




### -field hwndOwner

A handle to a window which should own any messages or dialog boxes the application receiving the notification might display.


### -field NetResource

Specifies the network resource to connect to. The valid fields are the same as for the 
<a href="https://msdn.microsoft.com/37a3988c-18ee-400a-85c3-cc3cbdf015ea">NPAddConnection</a> function.


### -field dwAddFlags

Any combination of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CONNECT_TEMPORARY"></a><a id="connect_temporary"></a><dl>
<dt><b>CONNECT_TEMPORARY</b></dt>
</dl>
</td>
<td width="60%">
The connection is being established for browsing purposes and may be released quickly.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_INTERACTIVE"></a><a id="connect_interactive"></a><dl>
<dt><b>CONNECT_INTERACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The connection may have interaction with the user.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_PROMPT"></a><a id="connect_prompt"></a><dl>
<dt><b>CONNECT_PROMPT</b></dt>
</dl>
</td>
<td width="60%">
Do not use any defaults without offering the user the chance to supply an alternative. This flag is  valid only if CONNECT_INTERACTIVE is set.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_UPDATE_PROFILE"></a><a id="connect_update_profile"></a><dl>
<dt><b>CONNECT_UPDATE_PROFILE</b></dt>
</dl>
</td>
<td width="60%">
The connection is being made persistent.

</td>
</tr>
<tr>
<td width="40%"><a id="CONNECT_UPDATE_RECENT"></a><a id="connect_update_recent"></a><dl>
<dt><b>CONNECT_UPDATE_RECENT</b></dt>
</dl>
</td>
<td width="60%">
The connection is being added to the recent connection list.

</td>
</tr>
</table>
 

