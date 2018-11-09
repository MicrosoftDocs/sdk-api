---
UID: NF:certcli.ICertRequest.RetrievePending
title: ICertRequest::RetrievePending
author: windows-sdk-content
description: Retrieves a certificate's disposition status from an earlier request that may have previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.
old-location: security\icertrequest2_retrievepending.htm
tech.root: seccrypto
ms.assetid: 07a9ac57-f90e-4c5c-b563-8aebbcf8f42e
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CCertRequest object [Security],RetrievePending method, ICertRequest interface [Security],RetrievePending method, ICertRequest.RetrievePending, ICertRequest2 interface [Security],RetrievePending method, ICertRequest2::RetrievePending, ICertRequest3 interface [Security],RetrievePending method, ICertRequest3::RetrievePending, ICertRequest::RetrievePending, RetrievePending, RetrievePending method [Security], RetrievePending method [Security],CCertRequest object, RetrievePending method [Security],ICertRequest interface, RetrievePending method [Security],ICertRequest2 interface, RetrievePending method [Security],ICertRequest3 interface, certcli/ICertRequest2::RetrievePending, certcli/ICertRequest3::RetrievePending, certcli/ICertRequest::RetrievePending, security.icertrequest2_retrievepending
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certcli.h
req.include-header: Certsrv.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest3.RetrievePending
 - ICertRequest2.RetrievePending
 - ICertRequest.RetrievePending
 - CCertRequest.RetrievePending
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest::RetrievePending


## -description


The <b>RetrievePending</b> method retrieves a certificate's disposition status from an earlier request that may have previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.

If the resulting disposition status is CR_DISP_ISSUED, you can retrieve the issued certificate by calling 
<a href="https://msdn.microsoft.com/ba8fc725-c376-4e66-8417-777ce13f2954">ICertRequest3::GetCertificate</a>. If a disposition other than CR_DISP_ISSUED is returned, call 
<a href="https://msdn.microsoft.com/ebe5cfa7-6bfd-4454-9272-64e3b1bf0ae2">ICertRequest3::GetLastStatus</a>, 
<a href="https://msdn.microsoft.com/c3639cf6-c70f-4f15-a0ed-e60abe2955cb">ICertRequest3::GetDispositionMessage</a>, or both methods for more information.


## -parameters




### -param RequestId [in]

The ID of the request that had previously returned CR_DISP_INCOMPLETE or CR_DISP_UNDER_SUBMISSION.


### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.


### -param pDisposition [out, retval]

A pointer to the request's disposition value.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this function, *<i>pDisposition</i> is set to one of the values in the following table.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value specifies the disposition of the request. The disposition is one of the following values.

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
Request did not complete

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Request failed

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Request denied

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_ISSUED_OUT_OF_BAND</b></dt>
</dl>
</td>
<td width="60%">
Certificate issued separately

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CR_DISP_UNDER_SUBMISSION</b></dt>
</dl>
</td>
<td width="60%">
Request taken under submission

</td>
</tr>
</table>
 




## -remarks



A successful call to this method generates an EXITEVENT_CERTRETRIEVEPENDING event. An active exit module will receive notification of this event (by means of a call to 
<a href="https://msdn.microsoft.com/ebe4ef0c-5778-4a62-b112-9b16b250814f">ICertExit3::Notify</a>) if the exit module specified this event when calling 
<a href="https://msdn.microsoft.com/61d27de8-f940-4f18-ba44-7e91378f035c">ICertExit3::Initialize</a>.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR    bstrCA = NULL;
long    nReqID, nDisp;

// In this example, the request ID is hard-coded.
nReqID = 1234;

// Note use of two '\' in C++ to produce one '\'.
bstrCA = SysAllocString(L"server01\\myCAName");

// pCertRequest is previously instantiated ICertRequest
// object pointer. Retrieve the status for the specified request.
hr = pCertRequest-&gt;RetrievePending( nReqID, bstrCA, &amp;nDisp );
if (FAILED(hr))
{
    printf("Failed RetrievePending [%x]\n", hr);
    goto error;
}
else
{
    // Use the disposition value as needed...
}
// Free BSTR resource.
if ( NULL != bstrCA )
    SysFreeString( bstrCA );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

