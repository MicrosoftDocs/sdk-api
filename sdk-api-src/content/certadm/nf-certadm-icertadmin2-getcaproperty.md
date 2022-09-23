---
UID: NF:certadm.ICertAdmin2.GetCAProperty
title: ICertAdmin2::GetCAProperty (certadm.h)
description: Retrieves a property value for the certification authority (CA). (ICertAdmin2.GetCAProperty)
helpviewer_keywords: ["CCertAdmin object [Security]","GetCAProperty method","CR_PROP_ADVANCEDSERVER","CR_PROP_BASECRL","CR_PROP_BASECRLPUBLISHSTATUS","CR_PROP_CABACKWARDCROSSCERT","CR_PROP_CABACKWARDCROSSCERTSTATE","CR_PROP_CACERTSTATE","CR_PROP_CACERTSTATUSCODE","CR_PROP_CACERTVERSION","CR_PROP_CAFORWARDCROSSCERT","CR_PROP_CAFORWARDCROSSCERTSTATE","CR_PROP_CANAME","CR_PROP_CASIGCERT","CR_PROP_CASIGCERTCHAIN","CR_PROP_CASIGCERTCOUNT","CR_PROP_CASIGCERTCRLCHAIN","CR_PROP_CATYPE","CR_PROP_CAXCHGCERT","CR_PROP_CAXCHGCERTCHAIN","CR_PROP_CAXCHGCERTCOUNT","CR_PROP_CAXCHGCERTCRLCHAIN","CR_PROP_CERTAIAURLS","CR_PROP_CERTCDPURLS","CR_PROP_CRLSTATE","CR_PROP_DELTACRL","CR_PROP_DELTACRLPUBLISHSTATUS","CR_PROP_DNSNAME","CR_PROP_EXITCOUNT","CR_PROP_EXITDESCRIPTION","CR_PROP_FILEVERSION","CR_PROP_KRACERT","CR_PROP_KRACERTCOUNT","CR_PROP_KRACERTSTATE","CR_PROP_KRACERTUSEDCOUNT","CR_PROP_PARENTCA","CR_PROP_POLICYDESCRIPTION","CR_PROP_PRODUCTVERSION","CR_PROP_ROLESEPARATIONENABLED","CR_PROP_SANITIZEDCANAME","CR_PROP_SANITIZEDCASHORTNAME","CR_PROP_SHAREDFOLDER","CR_PROP_TEMPLATES","CV_OUT_BASE64","CV_OUT_BASE64HEADER","CV_OUT_BASE64REQUESTHEADER","CV_OUT_BASE64X509CRLHEADER","CV_OUT_BINARY","CV_OUT_HEX","CV_OUT_HEXADDR","CV_OUT_HEXASCII","CV_OUT_HEXASCIIADDR","GetCAProperty","GetCAProperty method [Security]","GetCAProperty method [Security]","CCertAdmin object","GetCAProperty method [Security]","ICertAdmin2 interface","ICertAdmin2 interface [Security]","GetCAProperty method","ICertAdmin2.GetCAProperty","ICertAdmin2::GetCAProperty","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_icertadmin2_getcaproperty","certadm/ICertAdmin2::GetCAProperty","security.icertadmin2_getcaproperty"]
old-location: security\icertadmin2_getcaproperty.htm
tech.root: security
ms.assetid: 8eaa2e36-4358-4abd-a7c2-2c9768766597
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],GetCAProperty method, CR_PROP_ADVANCEDSERVER, CR_PROP_BASECRL, CR_PROP_BASECRLPUBLISHSTATUS, CR_PROP_CABACKWARDCROSSCERT, CR_PROP_CABACKWARDCROSSCERTSTATE, CR_PROP_CACERTSTATE, CR_PROP_CACERTSTATUSCODE, CR_PROP_CACERTVERSION, CR_PROP_CAFORWARDCROSSCERT, CR_PROP_CAFORWARDCROSSCERTSTATE, CR_PROP_CANAME, CR_PROP_CASIGCERT, CR_PROP_CASIGCERTCHAIN, CR_PROP_CASIGCERTCOUNT, CR_PROP_CASIGCERTCRLCHAIN, CR_PROP_CATYPE, CR_PROP_CAXCHGCERT, CR_PROP_CAXCHGCERTCHAIN, CR_PROP_CAXCHGCERTCOUNT, CR_PROP_CAXCHGCERTCRLCHAIN, CR_PROP_CERTAIAURLS, CR_PROP_CERTCDPURLS, CR_PROP_CRLSTATE, CR_PROP_DELTACRL, CR_PROP_DELTACRLPUBLISHSTATUS, CR_PROP_DNSNAME, CR_PROP_EXITCOUNT, CR_PROP_EXITDESCRIPTION, CR_PROP_FILEVERSION, CR_PROP_KRACERT, CR_PROP_KRACERTCOUNT, CR_PROP_KRACERTSTATE, CR_PROP_KRACERTUSEDCOUNT, CR_PROP_PARENTCA, CR_PROP_POLICYDESCRIPTION, CR_PROP_PRODUCTVERSION, CR_PROP_ROLESEPARATIONENABLED, CR_PROP_SANITIZEDCANAME, CR_PROP_SANITIZEDCASHORTNAME, CR_PROP_SHAREDFOLDER, CR_PROP_TEMPLATES, CV_OUT_BASE64, CV_OUT_BASE64HEADER, CV_OUT_BASE64REQUESTHEADER, CV_OUT_BASE64X509CRLHEADER, CV_OUT_BINARY, CV_OUT_HEX, CV_OUT_HEXADDR, CV_OUT_HEXASCII, CV_OUT_HEXASCIIADDR, GetCAProperty, GetCAProperty method [Security], GetCAProperty method [Security],CCertAdmin object, GetCAProperty method [Security],ICertAdmin2 interface, ICertAdmin2 interface [Security],GetCAProperty method, ICertAdmin2.GetCAProperty, ICertAdmin2::GetCAProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertadmin2_getcaproperty, certadm/ICertAdmin2::GetCAProperty, security.icertadmin2_getcaproperty
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Certidl.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertAdmin2::GetCAProperty
 - certadm/ICertAdmin2::GetCAProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.GetCAProperty
 - CCertAdmin.GetCAProperty
---

# ICertAdmin2::GetCAProperty


## -description

The <b>GetCAProperty</b> method retrieves a property value for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>GetCAProperty</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param PropId [in]

Specifies one of the following property identifiers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_ADVANCEDSERVER"></a><a id="cr_prop_advancedserver"></a><dl>
<dt><b>CR_PROP_ADVANCEDSERVER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Specifies whether the CA is running Advanced Server.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_BASECRL"></a><a id="cr_prop_basecrl"></a><dl>
<dt><b>CR_PROP_BASECRL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The CA's full, or base, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_BASECRLPUBLISHSTATUS"></a><a id="cr_prop_basecrlpublishstatus"></a><dl>
<dt><b>CR_PROP_BASECRLPUBLISHSTATUS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

The base CRL publish status. For more details, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CABACKWARDCROSSCERT"></a><a id="cr_prop_cabackwardcrosscert"></a><dl>
<dt><b>CR_PROP_CABACKWARDCROSSCERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The backward cross certificate. A backward cross certificate is the certificate issued upon renewal from the CA to itself signed with CA's new  key. The backward cross certificate has the authority key identifier of the new CA certificate and the subject key identifier of the old CA certificate.

 Applies to root CAs only.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CABACKWARDCROSSCERTSTATE"></a><a id="cr_prop_cabackwardcrosscertstate"></a><dl>
<dt><b>CR_PROP_CABACKWARDCROSSCERTSTATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

Whether the backward cross certificate is valid.  Valid for root CAs only.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CACERTSTATE"></a><a id="cr_prop_cacertstate"></a><dl>
<dt><b>CR_PROP_CACERTSTATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

State of the CA certificate. The values can be:<ul>
<li>CA_DISP_REVOKED</li>
<li>CA_DISP_VALID</li>
<li>CA_DISP_INVALID</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CACERTSTATUSCODE"></a><a id="cr_prop_cacertstatuscode"></a><dl>
<dt><b>CR_PROP_CACERTSTATUSCODE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

Status of the CA certificate, as an <b>HRESULT</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CACERTVERSION"></a><a id="cr_prop_cacertversion"></a><dl>
<dt><b>CR_PROP_CACERTVERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

Version of the CA certificate, as a DWORD. The high-order word is the key index, and the low-order word is the CA certificate index.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAFORWARDCROSSCERT"></a><a id="cr_prop_caforwardcrosscert"></a><dl>
<dt><b>CR_PROP_CAFORWARDCROSSCERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The forward cross certificate. A forward cross certificate is a certificate issued upon renewal from the CA to itself signed with CA's previous key. The forward cross certificate has the authority key identifier of the previous CA certificate and the subject key identifier of the new CA certificate.

 Applies to root CAs only. 

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAFORWARDCROSSCERTSTATE"></a><a id="cr_prop_caforwardcrosscertstate"></a><dl>
<dt><b>CR_PROP_CAFORWARDCROSSCERTSTATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

Whether the forward cross certificate is valid.  Valid for root CAs only.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CANAME"></a><a id="cr_prop_caname"></a><dl>
<dt><b>CR_PROP_CANAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

Name of the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CASIGCERT"></a><a id="cr_prop_casigcert"></a><dl>
<dt><b>CR_PROP_CASIGCERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

CA signing certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CASIGCERTCHAIN"></a><a id="cr_prop_casigcertchain"></a><dl>
<dt><b>CR_PROP_CASIGCERTCHAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

CA signing certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CASIGCERTCOUNT"></a><a id="cr_prop_casigcertcount"></a><dl>
<dt><b>CR_PROP_CASIGCERTCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Number of signing certificates for the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CASIGCERTCRLCHAIN"></a><a id="cr_prop_casigcertcrlchain"></a><dl>
<dt><b>CR_PROP_CASIGCERTCRLCHAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The CA's signing certificate CRL chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CATYPE"></a><a id="cr_prop_catype"></a><dl>
<dt><b>CR_PROP_CATYPE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Type of CA. This can be one of the following values (defined in Certsrv.h):<ul>
<li>ENUM_ENTERPRISE_ROOTCA</li>
<li>ENUM_ENTERPRISE_SUBCA</li>
<li>ENUM_STANDALONE_ROOTCA</li>
<li>ENUM_STANDALONE_SUBCA</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAXCHGCERT"></a><a id="cr_prop_caxchgcert"></a><dl>
<dt><b>CR_PROP_CAXCHGCERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

CA exchange certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAXCHGCERTCHAIN"></a><a id="cr_prop_caxchgcertchain"></a><dl>
<dt><b>CR_PROP_CAXCHGCERTCHAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

CA exchange certificate chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAXCHGCERTCOUNT"></a><a id="cr_prop_caxchgcertcount"></a><dl>
<dt><b>CR_PROP_CAXCHGCERTCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Number of exchange certificates for the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CAXCHGCERTCRLCHAIN"></a><a id="cr_prop_caxchgcertcrlchain"></a><dl>
<dt><b>CR_PROP_CAXCHGCERTCRLCHAIN</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The CA's exchange certificate CRL chain.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CERTAIAURLS"></a><a id="cr_prop_certaiaurls"></a><dl>
<dt><b>CR_PROP_CERTAIAURLS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String, indexed

Specifies Authority Information Access URLs as the type of URL requested by a client.

<b>Windows Server 2003:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CERTCDPURLS"></a><a id="cr_prop_certcdpurls"></a><dl>
<dt><b>CR_PROP_CERTCDPURLS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String, indexed

Specifies CRL Distribution Point URLs as the type of URL requested by a client.

<b>Windows Server 2003:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_CRLSTATE"></a><a id="cr_prop_crlstate"></a><dl>
<dt><b>CR_PROP_CRLSTATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

State of the CA's CRL. The values can be:<ul>
<li>CA_DISP_REVOKED</li>
<li>CA_DISP_VALID</li>
<li>CA_DISP_INVALID</li>
<li>CA_DISP_ERROR</li>
</ul>


</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_DELTACRL"></a><a id="cr_prop_deltacrl"></a><dl>
<dt><b>CR_PROP_DELTACRL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The CA's delta CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_DELTACRLPUBLISHSTATUS"></a><a id="cr_prop_deltacrlpublishstatus"></a><dl>
<dt><b>CR_PROP_DELTACRLPUBLISHSTATUS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

The delta CRL publish status. For more details, see Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_DNSNAME"></a><a id="cr_prop_dnsname"></a><dl>
<dt><b>CR_PROP_DNSNAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The CA's DNS Name.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_EXITCOUNT"></a><a id="cr_prop_exitcount"></a><dl>
<dt><b>CR_PROP_EXITCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Number of exit modules in use by the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_EXITDESCRIPTION"></a><a id="cr_prop_exitdescription"></a><dl>
<dt><b>CR_PROP_EXITDESCRIPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

Description for the exit module.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_FILEVERSION"></a><a id="cr_prop_fileversion"></a><dl>
<dt><b>CR_PROP_FILEVERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The Certificate Services file version.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERT"></a><a id="cr_prop_kracert"></a><dl>
<dt><b>CR_PROP_KRACERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Binary, indexed

The CA's key recovery agent (KRA) certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERTCOUNT"></a><a id="cr_prop_kracertcount"></a><dl>
<dt><b>CR_PROP_KRACERTCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Number of KRA certificates for the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERTSTATE"></a><a id="cr_prop_kracertstate"></a><dl>
<dt><b>CR_PROP_KRACERTSTATE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long, indexed

The KRA's certificate state. The return value is one of the following:

<ul>
<li>KRA_DISP_EXPIRED</li>
<li>KRA_DISP_NOTFOUND</li>
<li>KRA_DISP_REVOKED</li>
<li>KRA_DISP_VALID</li>
<li>KRA_DISP_UNTRUSTED</li>
<li>KRA_DISP_NOTLOADED</li>
<li>KRA_DISP_INVALID</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_KRACERTUSEDCOUNT"></a><a id="cr_prop_kracertusedcount"></a><dl>
<dt><b>CR_PROP_KRACERTUSEDCOUNT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Number of KRA certificates used by the CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_PARENTCA"></a><a id="cr_prop_parentca"></a><dl>
<dt><b>CR_PROP_PARENTCA</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The name of the CA's parent CA.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_POLICYDESCRIPTION"></a><a id="cr_prop_policydescription"></a><dl>
<dt><b>CR_PROP_POLICYDESCRIPTION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The description for the policy module.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_PRODUCTVERSION"></a><a id="cr_prop_productversion"></a><dl>
<dt><b>CR_PROP_PRODUCTVERSION</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The product version in which the file shipped.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_ROLESEPARATIONENABLED"></a><a id="cr_prop_roleseparationenabled"></a><dl>
<dt><b>CR_PROP_ROLESEPARATIONENABLED</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: Long

Value specifying whether role separation is enabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_SANITIZEDCANAME"></a><a id="cr_prop_sanitizedcaname"></a><dl>
<dt><b>CR_PROP_SANITIZEDCANAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The sanitized name of the CA. For a definition of a sanitized CA name, see <a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-getconfig">ICertConfig2::GetConfig</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_SANITIZEDCASHORTNAME"></a><a id="cr_prop_sanitizedcashortname"></a><dl>
<dt><b>CR_PROP_SANITIZEDCASHORTNAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The sanitized short name of the CA. For a definition of a sanitized CA short name, see <a href="/windows/desktop/api/certcli/nf-certcli-icertconfig-getconfig">ICertConfig2::GetConfig</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_SHAREDFOLDER"></a><a id="cr_prop_sharedfolder"></a><dl>
<dt><b>CR_PROP_SHAREDFOLDER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

The name of the shared folder directory.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_PROP_TEMPLATES"></a><a id="cr_prop_templates"></a><dl>
<dt><b>CR_PROP_TEMPLATES</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of the property: String

List of templates supported by the CA.

</td>
</tr>
</table>

### -param PropIndex [in]

If the <i>PropId</i> parameter is indexed, the zero-based index to use when retrieving the property value. If <i>PropId</i> is not indexed, this value is ignored.

### -param PropType [in]

Specifies the type of the property, indicated in the Meaning column of the <i>PropId</i> table. The type can be one of the following types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Signed long data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time (reserved for future use)

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string data

</td>
</tr>
</table>

### -param Flags [in]

The following flags can be used to specify the format of the returned property value; these flags have meaning only for binary data (such as certificates, certificate chains or <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a>) and is ignored otherwise.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64"></a><a id="cv_out_base64"></a><dl>
<dt><b>CV_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 without BEGIN/END

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64HEADER"></a><a id="cv_out_base64header"></a><dl>
<dt><b>CV_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN CERTIFICATE and END CERTIFICATE

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64REQUESTHEADER"></a><a id="cv_out_base64requestheader"></a><dl>
<dt><b>CV_OUT_BASE64REQUESTHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN NEW CERTIFICATE REQUEST and END NEW CERTIFICATE REQUEST

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64X509CRLHEADER"></a><a id="cv_out_base64x509crlheader"></a><dl>
<dt><b>CV_OUT_BASE64X509CRLHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN X509 CRL and END X509 CRL

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BINARY"></a><a id="cv_out_binary"></a><dl>
<dt><b>CV_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEX"></a><a id="cv_out_hex"></a><dl>
<dt><b>CV_OUT_HEX</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXADDR"></a><a id="cv_out_hexaddr"></a><dl>
<dt><b>CV_OUT_HEXADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with address/offset

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCII"></a><a id="cv_out_hexascii"></a><dl>
<dt><b>CV_OUT_HEXASCII</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCIIADDR"></a><a id="cv_out_hexasciiaddr"></a><dl>
<dt><b>CV_OUT_HEXASCIIADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII and address/offset

</td>
</tr>
</table>

### -param pvarPropertyValue [out]

A pointer to a buffer that receives the requested property value. It is a caller's responsibility to free this resource when done by calling <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>.

## -returns

<h3>C++</h3>
The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.

<h3>VB</h3>
The requested property value.

## -remarks

The following values are returned when the property identifier is CR_PROP_BASECRLPUBLISHSTATUS or CR_PROP_DELTACRLPUBLISHSTATUS. These values can be combined.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td> CPF_BADURL_ERROR</td>
<td>A URL is not valid.</td>
</tr>
<tr>
<td>CPF_BASE</td>
<td>A base CRL was published.</td>
</tr>
<tr>
<td>CPF_CASTORE_ERROR</td>
<td>A CA store error prevented publication.</td>
</tr>
<tr>
<td> CPF_COMPLETE</td>
<td>A complete CRL was published.</td>
</tr>
<tr>
<td>CPF_DELTA</td>
<td>A delta CRL was published.</td>
</tr>
<tr>
<td> CPF_FILE_ERROR</td>
<td>A file error prevented publication.</td>
</tr>
<tr>
<td>CPF_FTP_ERROR</td>
<td>An FTP  error prevented publication.</td>
</tr>
<tr>
<td>CPF_HTTP_ERROR</td>
<td>An HTTP error prevented publication.</td>
</tr>
<tr>
<td>CPF_LDAP_ERROR</td>
<td>An LDAP error prevented publication.</td>
</tr>
<tr>
<td>CPF_MANUAL</td>
<td>A CRL was published manually.</td>
</tr>
<tr>
<td> CPF_SHADOW</td>
<td>An empty delta CRL was published, along with a new BASE CRL.</td>
</tr>
<tr>
<td>CPF_SIGNATURE_ERROR</td>
<td>A signature error   prevented publication.</td>
</tr>
</table>
 

For an example of retrieving a CRL, see <a href="/windows/desktop/SecCrypto/retrieving-a-certificate-revocation-list">Retrieving a Certificate Revocation List</a>.


#### Examples

The following example shows retrieving the signature certificate of the CA. The  example assumes the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a> interface pointer is valid.


```cpp
BSTR bstrCA = NULL;
VARIANT var1;
HRESULT hr;

bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
if (NULL == bstrCA)
{
    printf("Failed to allocate memory for bstrCA\n");
    exit(1);
}

VariantInit(&var1);
// Retrieve the CA signature certificate at index 0.
hr = pAdmin2->GetCAProperty(bstrCA,
                                CR_PROP_CASIGCERT,
                                0,
                                PROPTYPE_BINARY,
                                CV_OUT_BASE64HEADER,
                                &var1);
if (FAILED(hr))
{
    printf("Failed GetCAProperty\n");
    SysFreeString(bstrCA);
    exit(1);  // Or other error action.
}

// Use the property as needed.
// ...

// Clear the variant when finished.
VariantClear(&var1);
SysFreeString(bstrCA);
```
