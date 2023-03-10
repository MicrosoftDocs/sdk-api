---
UID: NF:certadm.ICertAdmin.IsValidCertificate
title: ICertAdmin::IsValidCertificate (certadm.h)
description: Verifies the certificate against the certification authority (CA) key and checks that the certificate has not been revoked. This method was first defined in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin object [Security]","IsValidCertificate method","ICertAdmin interface [Security]","IsValidCertificate method","ICertAdmin.IsValidCertificate","ICertAdmin2 interface [Security]","IsValidCertificate method","ICertAdmin2::IsValidCertificate","ICertAdmin::IsValidCertificate","IsValidCertificate","IsValidCertificate method [Security]","IsValidCertificate method [Security]","CCertAdmin object","IsValidCertificate method [Security]","ICertAdmin interface","IsValidCertificate method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::IsValidCertificate","certadm/ICertAdmin::IsValidCertificate","security.icertadmin2_isvalidcertificate"]
old-location: security\icertadmin2_isvalidcertificate.htm
tech.root: security
ms.assetid: cd133c57-a62e-4083-b4fd-7eaf0c9e7606
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],IsValidCertificate method, ICertAdmin interface [Security],IsValidCertificate method, ICertAdmin.IsValidCertificate, ICertAdmin2 interface [Security],IsValidCertificate method, ICertAdmin2::IsValidCertificate, ICertAdmin::IsValidCertificate, IsValidCertificate, IsValidCertificate method [Security], IsValidCertificate method [Security],CCertAdmin object, IsValidCertificate method [Security],ICertAdmin interface, IsValidCertificate method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::IsValidCertificate, certadm/ICertAdmin::IsValidCertificate, security.icertadmin2_isvalidcertificate
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
 - ICertAdmin::IsValidCertificate
 - certadm/ICertAdmin::IsValidCertificate
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
 - ICertAdmin2.IsValidCertificate
 - ICertAdmin.IsValidCertificate
 - CCertAdmin.IsValidCertificate
---

# ICertAdmin::IsValidCertificate


## -description

The <b>IsValidCertificate</b> method verifies the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> against the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) key and  checks that the certificate has not been revoked. This method was first defined in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>IsValidCertificate</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param strSerialNumber [in]

Specifies a serial number that identifies the certificate to be reviewed. The string must specify the serial number as an even number of hexadecimal digits. If necessary, a zero can be prefixed to the number to produce an even number of digits. No more than one leading zero may be used.

### -param pDisposition [out, retval]

A pointer to a <b>LONG</b> that receives the disposition value.

## -returns

<h3>C++</h3>
 If the method succeeds and the <i>pDisposition</i> parameter is set to one of the following values, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the certificate. This value is one of the following values. (These values are defined in Certadm.h.)

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The call was not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The call failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_REVOKED</b></dt>
</dl>
</td>
<td width="60%">
The certificate has been revoked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_VALID</b></dt>
</dl>
</td>
<td width="60%">
The certificate is still valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The certificate was never issued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CA_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
The certificate is pending.

</td>
</tr>
</table>

## -remarks

This method determines only whether a certificate has been issued and is not currently revoked; it does not check that the current time and date are within the period for which the certificate is valid (the NotBefore and NotAfter certificate properties). An application that uses this method is also responsible for checking the certificate expiration.

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples


```cpp
    BSTR       bstrCA = NULL;      // Machine\CAName
    BSTR       bstrSerial = NULL;  // Contains the certificate 
                             // serial number
    long       nDisp;              // Contains the certificate
                             // disposition
    HRESULT    hr;

    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    bstrSerial = SysAllocString(L"<SERIALNUMBERHERE>");

    if (NULL == bstrCA || NULL == bstrSerial)
    {
        printf("Memory allocation failed\n");
        goto error;
    }

    //  Determine whether the certificate is valid.
    //  pCertAdmin is a previously instantiated ICertAdmin 
    //  object pointer.
    hr = pCertAdmin->IsValidCertificate(bstrCA, bstrSerial, &nDisp);
    if (FAILED(hr))
    {
        printf("Failed IsValidCertificate [%x]\n", hr);
        goto error;
    }
    //  Use nDisp as needed.

    //  Done processing.

error:

    //  Free BSTR values.
    if (NULL != bstrCA)
        SysFreeString(bstrCA);

    if (NULL != bstrSerial)
        SysFreeString(bstrSerial);
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>