---
UID: NS:winsafer._SAFER_URLZONE_IDENTIFICATION
title: SAFER_URLZONE_IDENTIFICATION (winsafer.h)
author: windows-sdk-content
description: Represents a URL zone identification rule.
old-location: security\safer_urlzone_identification.htm
tech.root: SecMgmt
ms.assetid: 8f165956-9ef0-469e-a71b-f9341a347e59
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSAFER_URLZONE_IDENTIFICATION, PSAFER_URLZONE_IDENTIFICATION, PSAFER_URLZONE_IDENTIFICATION structure pointer [Security], SAFER_URLZONE_IDENTIFICATION, SAFER_URLZONE_IDENTIFICATION structure [Security], URLZONE_INTERNET, URLZONE_INTRANET, URLZONE_LOCAL_MACHINE, URLZONE_TRUSTED, URLZONE_UNTRUSTED, _mnp_safer_urlzone_identification, security.safer_urlzone_identification, winsafer/PSAFER_URLZONE_IDENTIFICATION, winsafer/SAFER_URLZONE_IDENTIFICATION"
ms.topic: struct
req.header: winsafer.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinSafer.h
api_name:
 - SAFER_URLZONE_IDENTIFICATION
product: Windows
targetos: Windows
req.typenames: SAFER_URLZONE_IDENTIFICATION, *PSAFER_URLZONE_IDENTIFICATION
req.redist: 
---

# SAFER_URLZONE_IDENTIFICATION structure


## -description


The <b>SAFER_URLZONE_IDENTIFICATION</b> structure represents a URL zone identification rule.


## -struct-fields




### -field header

 


### -field UrlZoneId

A URLZONE identifier that represents the origin of the code image to be checked. The following table shows the possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="URLZONE_LOCAL_MACHINE"></a><a id="urlzone_local_machine"></a><dl>
<dt><b>URLZONE_LOCAL_MACHINE</b></dt>
</dl>
</td>
<td width="60%">
The local machine. 

</td>
</tr>
<tr>
<td width="40%"><a id="URLZONE_INTRANET"></a><a id="urlzone_intranet"></a><dl>
<dt><b>URLZONE_INTRANET</b></dt>
</dl>
</td>
<td width="60%">
The current intranet.

</td>
</tr>
<tr>
<td width="40%"><a id="URLZONE_TRUSTED"></a><a id="urlzone_trusted"></a><dl>
<dt><b>URLZONE_TRUSTED</b></dt>
</dl>
</td>
<td width="60%">
A trusted URL zone.

</td>
</tr>
<tr>
<td width="40%"><a id="URLZONE_INTERNET"></a><a id="urlzone_internet"></a><dl>
<dt><b>URLZONE_INTERNET</b></dt>
</dl>
</td>
<td width="60%">
The Internet.

</td>
</tr>
<tr>
<td width="40%"><a id="URLZONE_UNTRUSTED"></a><a id="urlzone_untrusted"></a><dl>
<dt><b>URLZONE_UNTRUSTED</b></dt>
</dl>
</td>
<td width="60%">
An untrusted URL zone.

</td>
</tr>
</table>
 


### -field dwSaferFlags

Reserved for future use.


#### - Header

A <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure containing the structure header. The <b>dwIdentificationType</b> member of the header must be <b>SaferIdentityTypeUrlZone</b>, and the <b>cbStructSize</b> member of the header must be sizeof(SAFER_URLZONE_IDENTIFICATION).

