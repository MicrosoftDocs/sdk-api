---
UID: NF:certadm.ICertAdmin2.PublishCRLs
title: ICertAdmin2::PublishCRLs
author: windows-sdk-content
description: Publishes certificate revocation lists (CRLs) for a certification authority (CA).
old-location: security\icertadmin2_publishcrls.htm
tech.root: seccrypto
ms.assetid: 27f9e991-bf2a-47f3-8f95-b56092fed7d0
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CA_CRL_BASE, CA_CRL_DELTA, CA_CRL_REPUBLISH, CCertAdmin2 object [Security],PublishCRLs method, ICertAdmin2 interface [Security],PublishCRLs method, ICertAdmin2.PublishCRLs, ICertAdmin2::PublishCRLs, PublishCRLs, PublishCRLs method [Security], PublishCRLs method [Security],CCertAdmin2 object, PublishCRLs method [Security],ICertAdmin2 interface, _certsrv_icertadmin2_publishcrls, certadm/ICertAdmin2::PublishCRLs, security.icertadmin2_publishcrls
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
 - ICertAdmin2.PublishCRLs
 - CCertAdmin2.PublishCRLs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin2::PublishCRLs


## -description


The <b>PublishCRLs</b> method  publishes <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate revocation lists</a> (CRLs) for a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a> (CA). This method was first defined in the <a href="https://msdn.microsoft.com/en-us/library/Aa383233(v=VS.85).aspx">ICertAdmin</a> interface.

The <b>PublishCRLs</b> method publishes a CRL based on the CA's current certificate, as well as CRLs based on any CA certificates that have been renewed and are not yet expired.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see <a href="https://msdn.microsoft.com/en-us/library/Aa383268(v=VS.85).aspx">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>PublishCRLs</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/en-us/library/Aa383234(v=VS.85).aspx">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param Date [in]

Specifies the next update value of the CRL in GMT time. 
If  <i>Date</i> is nonzero, the next update value for the CRL is <i>Date</i>, subject to  rounding or ceiling limits enforced by <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Services</a>. If <i>Date</i> is zero, the  next update value of the CRL is calculated from  the default CRL publication period.


### -param CRLFlags [in]

Value that specifies the CRL publishing options. This value can be a bitwise combination of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CA_CRL_BASE"></a><a id="ca_crl_base"></a><dl>
<dt><b>CA_CRL_BASE</b></dt>
</dl>
</td>
<td width="60%">
A base CRL is published, or the most recent base CRL is republished if CA_CRL_REPUBLISH is set.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_CRL_DELTA"></a><a id="ca_crl_delta"></a><dl>
<dt><b>CA_CRL_DELTA</b></dt>
</dl>
</td>
<td width="60%">
A delta CRL is published, or the most recent delta CRL is republished if CA_CRL_REPUBLISH is set. Note that if the CA has not enabled delta CRL publishing, use of this flag will result in an error.

</td>
</tr>
<tr>
<td width="40%"><a id="CA_CRL_REPUBLISH"></a><a id="ca_crl_republish"></a><dl>
<dt><b>CA_CRL_REPUBLISH</b></dt>
</dl>
</td>
<td width="60%">
The most recent  base or delta CRL, as specified by CA_CRL_BASE or CA_CRL_DELTA, is republished. The CA will not republish a CRL to a CRL distribution point if the CRL at the distribution point is already the most recent CRL.

</td>
</tr>
</table>
 


## -remarks



To determine whether a CA has successfully published base and delta CRLs, call <a href="https://msdn.microsoft.com/en-us/library/Aa383238(v=VS.85).aspx">ICertAdmin2::GetCAProperty</a> with the CR_PROP_BASECRLPUBLISHSTATUS and CR_PROP_DELTACRLPUBLISHSTATUS property identifiers, respectively.


#### Examples

The following example shows publishing CRLs.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    DATE ExpDate;  // CRL expiration date.
    SYSTEMTIME st;
    BSTR bstrCA = NULL;

    //  Set the CRL expiration date to noon, July 1, 2001.
    //  Zero out values first (avoids setting minutes,
    //  seconds, and so on).
    memset(&amp;st, 0, sizeof(SYSTEMTIME));
    st.wYear = 2001;
    st.wMonth = 7;     // July
    st.wDay = 1;       // first day of month
    st.wHour = 12;     // noon

    //  Place the date in required format.
    if (!SystemTimeToVariantTime(&amp;st, &amp;ExpDate))
    {
        printf("Unable to convert time\n");
        goto error;
    }

    bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
    if (NULL == bstrCA)
    {
        printf("Memory allocation failed\n");
        goto error;
    }

    //  Publish the CRL.
    //  pCertAdmin is a previously instantiated ICertAdmin object.
    hr = pCertAdmin2-&gt;PublishCRLs(bstrCA,
                              ExpDate,
                              CA_CRL_BASE);
    if (FAILED(hr))
    {
        printf("Failed PublishCRLs [%x]\n", hr);
        goto error;
    }
    else
        printf("PublishCRLs succeeded\n");
    //  Done.

error:

    //  Free resources.
    if (bstrCA)
        SysFreeString(bstrCA);</pre>
</td>
</tr>
</table></span></div>


