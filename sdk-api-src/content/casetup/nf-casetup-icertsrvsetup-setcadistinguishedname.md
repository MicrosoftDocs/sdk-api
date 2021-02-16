---
UID: NF:casetup.ICertSrvSetup.SetCADistinguishedName
title: ICertSrvSetup::SetCADistinguishedName (casetup.h)
description: Sets a certification authority (CA) common name and an optional distinguished name suffix.
helpviewer_keywords: ["ICertSrvSetup interface [Security]","SetCADistinguishedName method","ICertSrvSetup.SetCADistinguishedName","ICertSrvSetup::SetCADistinguishedName","SetCADistinguishedName","SetCADistinguishedName method [Security]","SetCADistinguishedName method [Security]","ICertSrvSetup interface","casetup/ICertSrvSetup::SetCADistinguishedName","security.icertsrvsetup_setcadistinguishedname"]
old-location: security\icertsrvsetup_setcadistinguishedname.htm
tech.root: security
ms.assetid: d513d4fd-abc7-44e6-822e-955de8613d55
ms.date: 12/05/2018
ms.keywords: ICertSrvSetup interface [Security],SetCADistinguishedName method, ICertSrvSetup.SetCADistinguishedName, ICertSrvSetup::SetCADistinguishedName, SetCADistinguishedName, SetCADistinguishedName method [Security], SetCADistinguishedName method [Security],ICertSrvSetup interface, casetup/ICertSrvSetup::SetCADistinguishedName, security.icertsrvsetup_setcadistinguishedname
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertSrvSetup::SetCADistinguishedName
 - casetup/ICertSrvSetup::SetCADistinguishedName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertSrvSetup.SetCADistinguishedName
---

# ICertSrvSetup::SetCADistinguishedName


## -description

The <b>SetCADistinguishedName</b> method sets a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) common name and an optional distinguished name suffix.

## -parameters

### -param bstrCADN [in]

A string that contains the name for a CA in the form <i>CommonName</i>,<i>DistinguishedNameSuffix</i>, where the comma (,) and <i>DistinguishedNameSuffix</i> are optional.


The following table describes an example of a distinguished name, including the optional distinguished name suffix, for the computer <i>MyServer</i>.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CN=mydomain-<i>MyServer</i>-CA</dt>
</dl>
</td>
<td width="60%">
Common name for the <i>MyServer</i> computer that belongs to the <i>MyDomain</i> domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>DC=<i>MyDomain</i>,DC=<i>MyCompany</i>,DC=com</dt>
</dl>
</td>
<td width="60%">
Distinguished name suffix (optional)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>CN=<i>MyDomain</i>-<i>MyServer</i>-CA,DC=<i>MyDomain</i>,DC=<i>MyCompany</i>,DC=com</dt>
</dl>
</td>
<td width="60%">
Distinguished name including the optional suffix

</td>
</tr>
</table>

### -param bIgnoreUnicode [in]

A value that indicates whether to allow Unicode encoding of the name information. A value of <b>VARIANT_TRUE</b> enables Unicode encoding.

### -param bOverwriteExistingKey [in]

A value that indicates whether to allow the name in <i>bstrCADN</i>, even though a <a href="/windows/desktop/SecGloss/p-gly">private key</a> with the same name exists on the computer. A value of <b>VARIANT_TRUE</b> enables the method to overwrite the existing key.

### -param bOverwriteExistingCAInDS [in]

A value that indicates whether to allow the name in <i>bstrCADN</i>, even though a CA with the same distinguished name exists in the directory service. A value of <b>VARIANT_TRUE</b> enables the method to overwrite the existing directory service entry.

## -remarks

Upon success, the <b>SetCADistinguishedName</b> method changes the <b>ENUM_SETUPPROP_CANAME</b> and <b>ENUM_SETUPPROP_CADSSUFFIX</b> property values to reflect the <i>bstrCADN</i> name. For more information about setup properties, see <a href="/windows/win32/api/casetup/ne-casetup-casetupproperty">CASetupProperty</a>.

Upon failure, the <b>SetCADistinguishedName</b> method might set additional error information in the <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorid">CAErrorId</a> and <a href="/windows/desktop/api/casetup/nf-casetup-icertsrvsetup-get_caerrorstring">CAErrorString</a> properties.

If an existing key and its associated certificate are being used to configure the CA, this method must not be called. If an existing key is being used  to configure the CA, without using the associated certificate, the common name in <i>bstrCADN</i> must match the <a href="/windows/desktop/SecGloss/s-gly">sanitized</a> <b>ContainerName</b> of the key. 

If <i>bstrCADN</i> includes UTF8 encoding, set the appropriate flag in CAPolicy.inf and place it in the  %windir%.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertsrvsetup">ICertSrvSetup</a>