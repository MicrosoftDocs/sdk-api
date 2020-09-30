---
UID: NF:xenroll.ICEnroll4.addBlobPropertyToCertificate
title: ICEnroll4::addBlobPropertyToCertificate (xenroll.h)
description: Adds a BLOB property to a certificate.
helpviewer_keywords: ["CERT_DESCRIPTION_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_RENEWAL_PROP_ID","CEnroll object [Security]","addBlobPropertyToCertificate method","ICEnroll4 interface [Security]","addBlobPropertyToCertificate method","ICEnroll4.addBlobPropertyToCertificate","ICEnroll4::addBlobPropertyToCertificate","addBlobPropertyToCertificate","addBlobPropertyToCertificate method [Security]","addBlobPropertyToCertificate method [Security]","CEnroll object","addBlobPropertyToCertificate method [Security]","ICEnroll4 interface","security.icenroll4_addblobpropertytocertificate","xenroll/ICEnroll4::addBlobPropertyToCertificate"]
old-location: security\icenroll4_addblobpropertytocertificate.htm
tech.root: security
ms.assetid: a21e2636-d49f-4490-867c-2ea95d7fdc69
ms.date: 12/05/2018
ms.keywords: CERT_DESCRIPTION_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_RENEWAL_PROP_ID, CEnroll object [Security],addBlobPropertyToCertificate method, ICEnroll4 interface [Security],addBlobPropertyToCertificate method, ICEnroll4.addBlobPropertyToCertificate, ICEnroll4::addBlobPropertyToCertificate, addBlobPropertyToCertificate, addBlobPropertyToCertificate method [Security], addBlobPropertyToCertificate method [Security],CEnroll object, addBlobPropertyToCertificate method [Security],ICEnroll4 interface, security.icenroll4_addblobpropertytocertificate, xenroll/ICEnroll4::addBlobPropertyToCertificate
req.header: xenroll.h
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll4::addBlobPropertyToCertificate
 - xenroll/ICEnroll4::addBlobPropertyToCertificate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.addBlobPropertyToCertificate
 - CEnroll.addBlobPropertyToCertificate
---

# ICEnroll4::addBlobPropertyToCertificate


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addBlobPropertyToCertificate</b> method adds a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> property to a certificate.

This property was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a> interface.

## -parameters

### -param lPropertyId [in]

The identifier of the <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> property to add to the certificate.

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

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>