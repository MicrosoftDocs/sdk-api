---
UID: NF:certadm.ICertAdmin.RevokeCertificate
title: ICertAdmin::RevokeCertificate
author: windows-sdk-content
description: Revokes a certificate either on a specified date or immediately. This method was first defined in the ICertAdmin interface.
old-location: security\icertadmin2_revokecertificate.htm
tech.root: seccrypto
ms.assetid: d44ff8c1-a248-4e2a-a73f-55fbea9fce03
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CCertAdmin interface [Security],RevokeCertificate method, CRL_REASON_AFFILIATION_CHANGED, CRL_REASON_CA_COMPROMISE, CRL_REASON_CERTIFICATE_HOLD, CRL_REASON_CESSATION_OF_OPERATION, CRL_REASON_KEY_COMPROMISE, CRL_REASON_SUPERSEDED, CRL_REASON_UNSPECIFIED, ICertAdmin interface [Security],RevokeCertificate method, ICertAdmin.RevokeCertificate, ICertAdmin2 interface [Security],RevokeCertificate method, ICertAdmin2::RevokeCertificate, ICertAdmin::RevokeCertificate, RevokeCertificate, RevokeCertificate method [Security], RevokeCertificate method [Security],CCertAdmin interface, RevokeCertificate method [Security],ICertAdmin interface, RevokeCertificate method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::RevokeCertificate, certadm/ICertAdmin::RevokeCertificate, security.icertadmin2_revokecertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - ICertAdmin2.RevokeCertificate
 - ICertAdmin.RevokeCertificate
 - CCertAdmin.RevokeCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin::RevokeCertificate


## -description


The <b>RevokeCertificate</b> method revokes a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> either on a specified date or immediately. This method was first defined in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.

 A revoked certificate will appear in a subsequent <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation lists</a> (CRLs), provided the revocation date is effective at the time the CRL was published.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>RevokeCertificate</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param strSerialNumber [in]

 Specifies a serial number that identifies the certificate to be revoked. The string must specify the serial number as an even number of hexadecimal digits. If necessary, a zero can be prefixed to the number to produce an even number of digits. However, no more than one leading zero may be used.


### -param Reason [in]

Specifies the reason for the revocation. 
			The following values (defined in Wincrypt.h) are 
			supported reason codes.



#### CRL_REASON_UNSPECIFIED (0)



#### CRL_REASON_KEY_COMPROMISE (1)



#### CRL_REASON_CA_COMPROMISE (2)



#### CRL_REASON_AFFILIATION_CHANGED (3)



#### CRL_REASON_SUPERSEDED (4)



#### CRL_REASON_CESSATION_OF_OPERATION (5)



#### CRL_REASON_CERTIFICATE_HOLD (6)

You can reinstate a certificate revoked with the CRL_REASON_CERTIFICATE_HOLD revocation reason code by calling <b>RevokeCertificate</b> with MAXDWORD as the <i>Reason</i> value. Note that if a certificate has been revoked with any reason code other than CRL_REASON_CERTIFICATE_HOLD, it cannot be reinstated.


### -param Date [in]

Specifies the date, in Coordinated Universal Time (Greenwich Mean Time), on which the revocation will become effective. The value zero indicates the current Coordinated Universal Time, causing a certificate to be revoked immediately. The value of <i>Date</i> appears in the <b>Effective Revocation Date</b> column of the revoked certificate (in the Certification Authority MMC snap-in).


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This method can be called more than once on the same certificate, which allows you to change the effective revocation date and revocation reason.

If a currently revoked certificate has CRL_REASON_CERTIFICATE_HOLD as its reason code, you can reinstate the certificate by calling <b>RevokeCertificate</b> with MAXDWORD (defined in Winnt.h) as the value for its reason code (the <i>Reason</i> parameter). After it is reinstated, the certificate will not appear in future CRLs.

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    BSTR bstrCA = NULL;
    BSTR bstrSerial = NULL;  // certificate serial number
    long nReason;
    DATE RevokeDate;         // revocation date
    SYSTEMTIME st;

    bstrSerial = SysAllocString(L"&lt;SERIALNUMBERHERE&gt;");
    bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
    if (NULL == bstrCA || NULL == bstrSerial)
    {
        printf("Memory allocation failed\n");
        goto error;
    }
    
    nReason = CRL_REASON_AFFILIATION_CHANGED;  // Defined
	                                      // in Wincrypt.h

    //  Specify when the cert should be revoked.
    //  Note: To revoke immediately, set RevokeDate to zero.
    //  This example sets the revoke date to noon on 1/1/2001.
    //  Zero out values first (avoids setting minutes, seconds,
    //  and so on).
    memset(&amp;st, 0, sizeof(SYSTEMTIME));
    st.wYear = 2001;
    st.wMonth = 1;     // Jan
    st.wDay = 1;       // 1st day of month
    st.wHour = 12;     // Noon

    //  Place the date in the required format.
    if (!SystemTimeToVariantTime(&amp;st, &amp;RevokeDate))
    {
        printf("Unable to convert time.\n");
        goto error;
    }

    //  Revoke the certificate.
    //  pCertAdmin is a previously instantiated ICertAdmin object.
    hr = pCertAdmin-&gt;RevokeCertificate( bstrCA,
                                        bstrSerial,
                                        nReason,
                                        RevokeDate );
    if (FAILED(hr))
    {
        printf("Failed RevokeCertificate. [%x]\n", hr);
        goto error;
    }
    else
        printf("Certificate %ws revoked.\n", bstrSerial );

    //  Done processing.

error:

    //  Free resources.
    if (bstrSerial)
        SysFreeString( bstrSerial );
    if (bstrCA)
        SysFreeString( bstrCA );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">CCertAdmin</a>



<a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a>



<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>
 

 

