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

# ICEnroll4::addBlobPropertyToCertificate


## -description


<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addBlobPropertyToCertificate</b> method adds a <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> property to a certificate.

This property was first defined in the <a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a> interface.


## -parameters




### -param lPropertyId [in]

The identifier of the <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> property to add to the certificate.


### -param lReserved [in]

This parameter is reserved and must be zero.


### -param bstrProperty [in]

The data associated with the BLOB property. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_PVK_FILE_PROP_ID_________"></a><a id="cert_pvk_file_prop_id_________"></a><dl>
<dt><b>CERT_PVK_FILE_PROP_ID
        </b></dt>
</dl>
</td>
<td width="60%">
The name of the file that contains the private key associated with the certificate's public key.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FRIENDLY_NAME_PROP_ID_________"></a><a id="cert_friendly_name_prop_id_________"></a><dl>
<dt><b>CERT_FRIENDLY_NAME_PROP_ID
        </b></dt>
</dl>
</td>
<td width="60%">
The display name for the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_DESCRIPTION_PROP_ID"></a><a id="cert_description_prop_id"></a><dl>
<dt><b>CERT_DESCRIPTION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
The property displayed by the certificate UI. This property allows the user to describe the certificate's use.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RENEWAL_PROP_ID"></a><a id="cert_renewal_prop_id"></a><dl>
<dt><b>CERT_RENEWAL_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
The hash of the renewed certificate.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>
 

 

