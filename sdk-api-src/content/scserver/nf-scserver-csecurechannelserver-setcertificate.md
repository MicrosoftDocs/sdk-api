---
UID: NF:scserver.CSecureChannelServer.SetCertificate
title: CSecureChannelServer::SetCertificate
author: windows-sdk-content
description: The SetCertificate method specifies the certificate and private key of the secure authenticated channel (SAC) server. Information about where to get this certificate is given in Tools for Development.
old-location: wmdm\csecurechannelserver_setcertificate.htm
tech.root: WMDM
ms.assetid: 9f12e32c-4904-4591-bc6e-38f507b0dcf6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],SetCertificate method, CSecureChannelServer.SetCertificate, CSecureChannelServer::SetCertificate, CSecureChannelServerSetCertificate, SetCertificate, SetCertificate method [windows Media Device Manager], SetCertificate method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::SetCertificate, wmdm.csecurechannelserver_setcertificate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: scserver.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelServer.SetCertificate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- scserver.h
: 
- CSecureChannelServer.SetCertificate
: 
---

# CSecureChannelServer::SetCertificate


## -description



The <b>SetCertificate</b> method specifies the certificate and private key of the secure authenticated channel (SAC) server. Information about where to get this certificate is given in <a href="https://msdn.microsoft.com/7932f599-a073-4fc8-82da-c0e7001c1809">Tools for Development</a>.




## -parameters




### -param dwFlags [in]

Specifies the type of certificate being passed to this method. Must be set to SAC_CERT_V1.


### -param pbAppCert [in]

Pointer to the first byte of the certificate of the SAC client.


### -param dwCertLen [in]

<b>DWORD</b> specifying the length of the certificate to which <i>pbAppCert</i> points.


### -param pbAppPVK [in]

Pointer to the first byte of the private key of the SAC client.


### -param dwPVKLen [in]

<b>DWORD</b> specifying the length of the private key to which <i>pbAppPVK</i> points.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



This method sends the component's authentication certificate to <b>CSecureChannelClient</b>. <b>SetCertificate</b> should be called immediately after creating the <b>CSecureChannelServer</b> object. If <i>pbAppCert</i> and/or <i>pbAppPVK</i> are <b>NULL</b> (or both zero) a default certificate and private key pair is used which will allow for basic functionality.


#### Examples

The following code demonstrates creating a CSecureChannelServer object and setting its certificate. In this code, the variables <i>pbAppCert</i> and <i>pbAppPVK</i> are a matching certificate/key pair.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
extern CSecureChannelServer *g_pSCWMDM;
g_pSCWMDM = new CSecureChannelServer();

// Select the certificate and the associated private key into the SAC.
if (g_pSCWMDM)
{
    g_pSCWMDM-&gt;SetCertificate( SAC_CERT_V1, 
                               (BYTE*)g_abAppCert,
                               sizeof(g_abAppCert), 
                               (BYTE*)g_abPriv,
                               sizeof(g_abPriv) );
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>
 

 

