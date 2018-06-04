---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _SAFER_URLZONE_IDENTIFICATION structure


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

