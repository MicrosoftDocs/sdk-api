---
UID: NF:certcli.ICertRequest.GetCACertificate
title: ICertRequest::GetCACertificate
author: windows-sdk-content
description: Returns the certification authority (CA) certificate for the Certificate Services server.
old-location: security\icertrequest2_getcacertificate.htm
tech.root: seccrypto
ms.assetid: 711fdcec-0a07-4559-a577-1eb73053dd38
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CCertRequest object [Security],GetCACertificate method, CR_OUT_BASE64, CR_OUT_BASE64HEADER, CR_OUT_BINARY, CR_OUT_CHAIN, GetCACertificate, GetCACertificate method [Security], GetCACertificate method [Security],CCertRequest object, GetCACertificate method [Security],ICertRequest interface, GetCACertificate method [Security],ICertRequest2 interface, GetCACertificate method [Security],ICertRequest3 interface, ICertRequest interface [Security],GetCACertificate method, ICertRequest.GetCACertificate, ICertRequest2 interface [Security],GetCACertificate method, ICertRequest2::GetCACertificate, ICertRequest3 interface [Security],GetCACertificate method, ICertRequest3::GetCACertificate, ICertRequest::GetCACertificate, certcli/ICertRequest2::GetCACertificate, certcli/ICertRequest3::GetCACertificate, certcli/ICertRequest::GetCACertificate, security.icertrequest2_getcacertificate
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
 - ICertRequest3.GetCACertificate
 - ICertRequest2.GetCACertificate
 - ICertRequest.GetCACertificate
 - CCertRequest.GetCACertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertRequest::GetCACertificate


## -description


The <b>GetCACertificate</b> method returns the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) certificate for the Certificate Services server.


## -parameters




### -param fExchangeCertificate [in]

A Boolean value that specifies which CA certificate to return. If <i>fExchangeCertificate</i> is set to <b>false</b>, the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">signature certificate</a> of the CA will be returned. The Signature certificate of the CA can be used to verify signatures on certificates issued by the CA.

<b>Windows Server 2003:  </b>If <i>fExchangeCertificate</i> is set to <b>true</b>, the Exchange certificate of the CA will be returned. The Exchange certificate of the CA can be used to encrypt requests sent to the CA.

Beginning with Windows 7 and Windows Server 2008 R2, this parameter is ignored during https:// enrollment and the function, if successful, always returns the CA exchange certificate. To retrieve the CA signing certificate for an enrollment web service, use the <a href="https://msdn.microsoft.com/4588891e-7be4-482a-bbad-c23759b06b1b">Property</a> method on the <a href="https://msdn.microsoft.com/ffd64396-a258-4cf5-aca1-a61102ecf313">ICertificationAuthority</a> interface with the CAPropCertificate <a href="https://msdn.microsoft.com/d4908ef0-aaf0-4396-9b89-cd7f3a9f6188">EnrollmentCAProperty</a> enumeration value.

Note that <b>TRUE</b> is defined (in a Microsoft header file) for C/C++ programmers as one, while  Visual Basic defines the <b>True</b> keyword as negative one. As a result, Visual Basic developers must use one (instead of <b>True</b>) to set this parameter to <b>TRUE</b>. However, to set this parameter to <b>FALSE</b>, Visual Basic developers can use zero or <b>False</b>.


### -param strConfig [in]

Represents a valid configuration string for the Certificate Services server. The string can be either an HTTPS URL for an enrollment server or in the form <i>ComputerName</i><b>\</b><i>CAName</i>, where <i>ComputerName</i> is the network name of the server, and <i>CAName</i> is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>An HTTPS URL is not supported as an input.


### -param Flags [in]

The following flags can be used to specify the format of the returned certificate.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64HEADER"></a><a id="cr_out_base64header"></a><dl>
<dt><b>CR_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format with begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BASE64"></a><a id="cr_out_base64"></a><dl>
<dt><b>CR_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 format without begin/end.

</td>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_BINARY"></a><a id="cr_out_binary"></a><dl>
<dt><b>CR_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary format.

</td>
</tr>
</table>
 


The following flag can be combined with the format flag to specify that the complete certificate chain should be included with the requested CA certificate. Otherwise, just the requested CA certificate (in <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> format) is returned.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CR_OUT_CHAIN"></a><a id="cr_out_chain"></a><dl>
<dt><b>CR_OUT_CHAIN</b></dt>
</dl>
</td>
<td width="60%">
Include complete certificate chain in a PKCS #7.

</td>
</tr>
</table>
 


### -param pstrCertificate [out, retval]

A pointer to the <b>BSTR</b> that contains the CA certificate for the Certificate Services server, in the specified format.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

Upon successful completion of this method, *<i>pstrCertificate</i> is set to the <b>BSTR</b> that contains the CA certificate. To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrCertificate</i>.

  When you have finished using *<i>pstrCertificate</i>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The CA certificate for the Certificate Services server, in the specified format.




## -remarks



Administration tasks use DCOM. Code that calls this interface method as defined in an earlier version of Certadm.h will run on Windows-based servers as long as the client and the server are both running the same Windows operating system.




## -see-also




<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">CCertRequest</a>



<a href="https://msdn.microsoft.com/2f371aa6-492e-41ba-8455-66e9d5f5da44">ICertRequest</a>



<a href="https://msdn.microsoft.com/8587a682-27a5-4f26-b4bb-7088e4e5d8d3">ICertRequest2</a>



<a href="https://msdn.microsoft.com/01de2ac0-4844-41a6-acef-e3e83b350393">ICertRequest3</a>
 

 

