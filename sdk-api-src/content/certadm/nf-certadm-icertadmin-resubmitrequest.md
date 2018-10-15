---
UID: NF:certadm.ICertAdmin.ResubmitRequest
title: ICertAdmin::ResubmitRequest
author: windows-sdk-content
description: Submits the specified certificate request to the policy module for the specified certification authority. This method was first introduced in the ICertAdmin interface.
old-location: security\icertadmin2_resubmitrequest.htm
tech.root: seccrypto
ms.assetid: 610712d9-3661-42ba-9d2f-27862ba8dbd4
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CCertAdmin object [Security],ResubmitRequest method, ICertAdmin interface [Security],ResubmitRequest method, ICertAdmin.ResubmitRequest, ICertAdmin2 interface [Security],ResubmitRequest method, ICertAdmin2::ResubmitRequest, ICertAdmin::ResubmitRequest, ResubmitRequest, ResubmitRequest method [Security], ResubmitRequest method [Security],CCertAdmin object, ResubmitRequest method [Security],ICertAdmin interface, ResubmitRequest method [Security],ICertAdmin2 interface, certadm/ICertAdmin2::ResubmitRequest, certadm/ICertAdmin::ResubmitRequest, security.icertadmin2_resubmitrequest
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
 - ICertAdmin2.ResubmitRequest
 - ICertAdmin.ResubmitRequest
 - CCertAdmin.ResubmitRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertAdmin::ResubmitRequest


## -description


The <b>ResubmitRequest</b> method submits the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> to the 
<a href="https://msdn.microsoft.com/23d920ea-af62-42ce-ad48-c7a03ab55fc9">policy module</a> for the specified <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>. This method was first introduced in the <a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a> interface.

For this method to succeed, the certificate request must be pending.


## -parameters




### -param strConfig [in]

Represents a valid configuration string for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the network name of the Certificate Services server and CANAME is the common name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<div class="alert"><b>Important</b>  <b>ResubmitRequest</b> does not clear the internal cache when the configuration string is changed. When you change the configuration string for the CA, you must instantiate a new <a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin</a> object and call this method again with the new configuration string.</div>
<div> </div>

### -param RequestId [in]

Specifies the ID of the request to resubmit.


### -param pDisposition [out, retval]

A pointer to the disposition of the request.


## -returns



<h3>C++</h3>
 If the method succeeds and the <i>pDisposition</i> parameter is set to one of the following values that specify the disposition of the request, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the request. This value is one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The request was not completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The request failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The request was denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
The certificate was issued.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
The certificate was issued separately.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
The request was taken under submission.

</td>
</tr>
</table>
 




## -remarks



Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;Certadm.h&gt;


    long nDisp;  // disposition value
    long nReqID = &lt;REQUESTIDHERE&gt;;
    BSTR bstrCA = NULL;

    bstrCA = SysAllocString(L"&lt;COMPUTERNAMEHERE&gt;\\&lt;CANAMEHERE&gt;");
    if (NULL == bstrCA)
    {
        printf("Memory allocation failed\n");
        goto error;
    }

    //  pCertAdmin is a previously instantiated ICertAdmin object.
    hr = pCertAdmin-&gt;ResubmitRequest(bstrCA, nReqID, &amp;nDisp);
    if (FAILED(hr))
    {
        printf("Failed ResubmitRequest [%x]\n", hr);
        goto error;
    }
    else
        printf("ResubmitRequest disposition is %d\n", nDisp);

error:
    //  Free resources.
    if (bstrCA)
        SysFreeString(bstrCA);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">CCertAdmin</a>



<a href="https://msdn.microsoft.com/e906b69b-5574-4dd5-aa30-9c2a67972202">ICertAdmin</a>



<a href="https://msdn.microsoft.com/df40b6ac-825d-4e8d-a80b-6e57a4e740a2">ICertAdmin2</a>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/22ae8d39-3f16-4f7d-94a0-aa68b03aaa0b">ICertRequest::Submit</a>
 

 

