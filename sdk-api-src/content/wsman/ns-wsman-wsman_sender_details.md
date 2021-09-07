---
UID: NS:wsman._WSMAN_SENDER_DETAILS
title: WSMAN_SENDER_DETAILS (wsman.h)
description: Specifies the client details for every inbound request.
helpviewer_keywords: ["WSMAN_SENDER_DETAILS","WSMAN_SENDER_DETAILS structure [Windows Remote Management]","winrm.wsman_sender_details","wsman/WSMAN_SENDER_DETAILS"]
old-location: winrm\wsman_sender_details.htm
tech.root: winrm
ms.assetid: f68a9f75-6808-4dfa-b40f-061da88ead3c
ms.date: 12/05/2018
ms.keywords: WSMAN_SENDER_DETAILS, WSMAN_SENDER_DETAILS structure [Windows Remote Management], winrm.wsman_sender_details, wsman/WSMAN_SENDER_DETAILS
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: WSMAN_SENDER_DETAILS
req.redist: Windows Management Framework on Windows Server 2008 with SP2, Windows Vista with SP1, and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - _WSMAN_SENDER_DETAILS
 - wsman/_WSMAN_SENDER_DETAILS
 - WSMAN_SENDER_DETAILS
 - wsman/WSMAN_SENDER_DETAILS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSMAN_SENDER_DETAILS
---

# WSMAN_SENDER_DETAILS structure


## -description

Specifies the client details for every inbound request.

## -struct-fields

### -field senderName

Specifies the user name of the client making the request.  The content of this parameter varies depending on the type of authentication. The value of the <i>senderName</i> is formatted as follows:

<table>
<tr>
<th>Authentication mechanism</th>
<th>Value of <i>senderName</i></th>
</tr>
<tr>
<td>
Windows Authentication

</td>
<td>
The domain and user name.

</td>
</tr>
<tr>
<td>
Basic Authentication

</td>
<td>
The user name specified.

</td>
</tr>
<tr>
<td>
Client Certificates

</td>
<td>
The subject of the certificate.

</td>
</tr>
<tr>
<td>
LiveID

</td>
<td>
The LiveID PUID as a string.

</td>
</tr>
</table>

### -field authenticationMechanism

Specifies a string that indicates which authentication mechanism was used by the client.  The following values are predefined:

<ul>
<li>Basic</li>
<li>ClientCertificate</li>
</ul>
All other types are queried directly from the security package.  For Internet Information Services (IIS) hosting, this string is retrieved from the IIS infrastructure.

### -field certificateDetails

A pointer to a <a href="/windows/desktop/api/wsman/ns-wsman-wsman_certificate_details">WSMAN_CERTIFICATE_DETAILS</a> structure that specifies the details of the client's certificate. This parameter is valid only if the <i>authenticationMechanism</i> is set to ClientCertificate.

### -field clientToken

Specifies the identity token of the user if a Windows security token is available for a user. This token will be used by the thread to impersonate this user for all calls into the plug-in.

<div class="alert"><b>Note</b>  Authorization plug-ins can change the user context and use a different impersonation token.</div>
<div> </div>

### -field httpURL

Specifies the HTTP URL of the inbound request.