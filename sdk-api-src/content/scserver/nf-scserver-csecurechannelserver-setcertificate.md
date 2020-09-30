---
UID: NF:scserver.CSecureChannelServer.SetCertificate
title: CSecureChannelServer::SetCertificate (scserver.h)
description: The SetCertificate method specifies the certificate and private key of the secure authenticated channel (SAC) server. Information about where to get this certificate is given in Tools for Development.
helpviewer_keywords: ["CSecureChannelServer class [windows Media Device Manager]","SetCertificate method","CSecureChannelServer.SetCertificate","CSecureChannelServer::SetCertificate","CSecureChannelServerSetCertificate","SetCertificate","SetCertificate method [windows Media Device Manager]","SetCertificate method [windows Media Device Manager]","CSecureChannelServer class","scserver/CSecureChannelServer::SetCertificate","wmdm.csecurechannelserver_setcertificate"]
old-location: wmdm\csecurechannelserver_setcertificate.htm
tech.root: WMDM
ms.assetid: 9f12e32c-4904-4591-bc6e-38f507b0dcf6
ms.date: 12/05/2018
ms.keywords: CSecureChannelServer class [windows Media Device Manager],SetCertificate method, CSecureChannelServer.SetCertificate, CSecureChannelServer::SetCertificate, CSecureChannelServerSetCertificate, SetCertificate, SetCertificate method [windows Media Device Manager], SetCertificate method [windows Media Device Manager],CSecureChannelServer class, scserver/CSecureChannelServer::SetCertificate, wmdm.csecurechannelserver_setcertificate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CSecureChannelServer::SetCertificate
 - scserver/CSecureChannelServer::SetCertificate
dev_langs:
 - c++
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
---

# CSecureChannelServer::SetCertificate


## -description

The <b>SetCertificate</b> method specifies the certificate and private key of the secure authenticated channel (SAC) server. Information about where to get this certificate is given in <a href="/windows/desktop/WMDM/tools-for-development">Tools for Development</a>.

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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

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


```cpp

extern CSecureChannelServer *g_pSCWMDM;
g_pSCWMDM = new CSecureChannelServer();

// Select the certificate and the associated private key into the SAC.
if (g_pSCWMDM)
{
    g_pSCWMDM->SetCertificate( SAC_CERT_V1, 
                               (BYTE*)g_abAppCert,
                               sizeof(g_abAppCert), 
                               (BYTE*)g_abPriv,
                               sizeof(g_abPriv) );
}

```

## -see-also

<a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer Class</a>