---
UID: NF:certadm.ICertAdmin.PublishCRL
title: ICertAdmin::PublishCRL
author: windows-sdk-content
description: Sends a request to the Certificate Services certification authority (CA) to publish a new certificate revocation list (CRL). This method was first introduced in the ICertAdmin interface.
old-location: security\icertadmin2_publishcrl.htm
tech.root: SecCrypto
ms.assetid: a42cab2d-2309-43f1-8d67-adbc5923ec45
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertAdmin object [Security],PublishCRL method, ICertAdmin interface [Security],PublishCRL method, ICertAdmin.PublishCRL, ICertAdmin2 interface [Security],PublishCRL method, ICertAdmin2::PublishCRL, ICertAdmin::PublishCRL, PublishCRL, PublishCRL method [Security], PublishCRL method [Security],CCertAdmin object, PublishCRL method [Security],ICertAdmin interface, PublishCRL method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::PublishCRL, certadm/ICertAdmin::PublishCRL, security.icertadmin2_publishcrl
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
 - ICertAdmin2.PublishCRL
 - ICertAdmin.PublishCRL
 - CCertAdmin.PublishCRL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin::PublishCRL


## -description


The <b>PublishCRL</b> method sends a request to the Certificate Services <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) to publish a new <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL). This method was first introduced in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see <a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.<div class="alert"><b>Important</b>  <b>PublishCRL</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>



### -param Date [in]

Specifies the next update value of the CRL in Coordinated Universal Time (Greenwich Mean Time). 
If  <i>Date</i> is nonzero, the next update value for the CRL is <i>Date</i>, subject to  rounding or ceiling limits enforced by Certificate Services. If <i>Date</i> is zero, the  next update value of the CRL is calculated from  the default CRL publication period.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

The following example shows publishing a CRL.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    DATE ExpDate;  // CRL expiration date
    SYSTEMTIME st;
    BSTR bstrCA = NULL;

    //  Set the CRL Expiration Date to Noon on Jan. 1, 2005 GMT.
    //  Zero out values first 
	//  (avoids setting minutes, seconds, and so on).
    memset(&amp;st, 0, sizeof(SYSTEMTIME));
    st.wYear = 2005;
    st.wMonth = 1;     // Jan
    st.wDay = 1;       // 1st day of month
    st.wHour = 12;     // Noon

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
    hr = pCertAdmin-&gt;PublishCRL(bstrCA, ExpDate);
    if (FAILED(hr))
    {
        printf("Failed PublishCRL [%x]\n", hr);
        goto error;
    }
    else
        printf("PublishCRL succeeded\n");</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">CCertAdmin</a>



<a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a>



<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>
 

 

