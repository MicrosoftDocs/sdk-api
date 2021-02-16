---
UID: NF:certadm.ICertAdmin.PublishCRL
title: ICertAdmin::PublishCRL (certadm.h)
description: Sends a request to the Certificate Services certification authority (CA) to publish a new certificate revocation list (CRL). This method was first introduced in the ICertAdmin interface.
helpviewer_keywords: ["CCertAdmin object [Security]","PublishCRL method","ICertAdmin interface [Security]","PublishCRL method","ICertAdmin.PublishCRL","ICertAdmin2 interface [Security]","PublishCRL method","ICertAdmin2::PublishCRL","ICertAdmin::PublishCRL","PublishCRL","PublishCRL method [Security]","PublishCRL method [Security]","CCertAdmin object","PublishCRL method [Security]","ICertAdmin interface","PublishCRL method [Security]","ICertAdmin2 interface","certadm/ICertAdmin2::PublishCRL","certadm/ICertAdmin::PublishCRL","security.icertadmin2_publishcrl"]
old-location: security\icertadmin2_publishcrl.htm
tech.root: security
ms.assetid: a42cab2d-2309-43f1-8d67-adbc5923ec45
ms.date: 12/05/2018
ms.keywords: CCertAdmin object [Security],PublishCRL method, ICertAdmin interface [Security],PublishCRL method, ICertAdmin.PublishCRL, ICertAdmin2 interface [Security],PublishCRL method, ICertAdmin2::PublishCRL, ICertAdmin::PublishCRL, PublishCRL, PublishCRL method [Security], PublishCRL method [Security],CCertAdmin object, PublishCRL method [Security],ICertAdmin interface, PublishCRL method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::PublishCRL, certadm/ICertAdmin::PublishCRL, security.icertadmin2_publishcrl
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
 - ICertAdmin::PublishCRL
 - certadm/ICertAdmin::PublishCRL
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
 - ICertAdmin2.PublishCRL
 - ICertAdmin.PublishCRL
 - CCertAdmin.PublishCRL
---

# ICertAdmin::PublishCRL


## -description

The <b>PublishCRL</b> method sends a request to the Certificate Services <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) to publish a new <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL). This method was first introduced in the <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a> interface.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see <a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.<div class="alert"><b>Important</b>  <b>PublishCRL</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param Date [in]

Specifies the next update value of the CRL in Coordinated Universal Time (Greenwich Mean Time). 
If  <i>Date</i> is nonzero, the next update value for the CRL is <i>Date</i>, subject to  rounding or ceiling limits enforced by Certificate Services. If <i>Date</i> is zero, the  next update value of the CRL is calculated from  the default CRL publication period.

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

The following example shows publishing a CRL.


```cpp
    DATE ExpDate;  // CRL expiration date
    SYSTEMTIME st;
    BSTR bstrCA = NULL;

    //  Set the CRL Expiration Date to Noon on Jan. 1, 2005 GMT.
    //  Zero out values first 
	//  (avoids setting minutes, seconds, and so on).
    memset(&st, 0, sizeof(SYSTEMTIME));
    st.wYear = 2005;
    st.wMonth = 1;     // Jan
    st.wDay = 1;       // 1st day of month
    st.wHour = 12;     // Noon

    //  Place the date in required format.
    if (!SystemTimeToVariantTime(&st, &ExpDate))
    {
        printf("Unable to convert time\n");
        goto error;
    }

    bstrCA = SysAllocString(L"<COMPUTERNAMEHERE>\\<CANAMEHERE>");
    if (NULL == bstrCA)
    {
        printf("Memory allocation failed\n");
        goto error;
    }

    //  Publish the CRL.
    //  pCertAdmin is a previously instantiated ICertAdmin object.
    hr = pCertAdmin->PublishCRL(bstrCA, ExpDate);
    if (FAILED(hr))
    {
        printf("Failed PublishCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("PublishCRL succeeded\n");
```

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">CCertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin">ICertAdmin</a>



<a href="/windows/desktop/api/certadm/nn-certadm-icertadmin2">ICertAdmin2</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>