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

# _WSMAN_SENDER_DETAILS structure


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

A pointer to a <a href="https://msdn.microsoft.com/82b723fd-c9bb-4ddd-bd2a-4b6d1186846b">WSMAN_CERTIFICATE_DETAILS</a> structure that specifies the details of the client's certificate. This parameter is valid only if the <i>authenticationMechanism</i>
 is set to ClientCertificate.


### -field clientToken

Specifies the identity token of the user if a Windows security token is available for a user. This token will be used by the thread to impersonate this user for all calls into the plug-in.

<div class="alert"><b>Note</b>  Authorization plug-ins can change the user context and use a different impersonation token.</div>
<div> </div>

### -field httpURL

Specifies the HTTP URL of the inbound request.

