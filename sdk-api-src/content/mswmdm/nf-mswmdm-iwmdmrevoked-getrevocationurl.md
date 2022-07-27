---
UID: NF:mswmdm.IWMDMRevoked.GetRevocationURL
title: IWMDMRevoked::GetRevocationURL (mswmdm.h)
description: The GetRevocationURL method retrieves the URL from which updated components can be downloaded. (IWMDMRevoked.GetRevocationURL)
helpviewer_keywords: ["GetRevocationURL","GetRevocationURL method [windows Media Device Manager]","GetRevocationURL method [windows Media Device Manager]","IWMDMRevoked interface","IWMDMRevoked interface [windows Media Device Manager]","GetRevocationURL method","IWMDMRevoked.GetRevocationURL","IWMDMRevoked::GetRevocationURL","IWMDMRevokedGetRevocationURL","mswmdm/IWMDMRevoked::GetRevocationURL","wmdm.iwmdmrevoked_getrevocationurl"]
old-location: wmdm\iwmdmrevoked_getrevocationurl.htm
tech.root: WMDM
ms.assetid: 0158a664-8f0b-4481-8028-46b05776a482
ms.date: 12/05/2018
ms.keywords: GetRevocationURL, GetRevocationURL method [windows Media Device Manager], GetRevocationURL method [windows Media Device Manager],IWMDMRevoked interface, IWMDMRevoked interface [windows Media Device Manager],GetRevocationURL method, IWMDMRevoked.GetRevocationURL, IWMDMRevoked::GetRevocationURL, IWMDMRevokedGetRevocationURL, mswmdm/IWMDMRevoked::GetRevocationURL, wmdm.iwmdmrevoked_getrevocationurl
req.header: mswmdm.h
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
 - IWMDMRevoked::GetRevocationURL
 - mswmdm/IWMDMRevoked::GetRevocationURL
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
 - IWMDMRevoked.GetRevocationURL
---

# IWMDMRevoked::GetRevocationURL


## -description

The <b>GetRevocationURL</b> method retrieves the URL from which updated components can be downloaded.

## -parameters

### -param ppwszRevocationURL [in, out]

Pointer to a string containing a revocation URL. This buffer is created and freed by the caller.

### -param pdwBufferLen [in, out]

Size of the buffer holding the revocation URL.

### -param pdwRevokedBitFlag [out]

Pointer to a <b>DWORD</b> specifying information on what component(s) have been revoked. This should be one or more of the following values, combined using a bitwise <b>OR</b>.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_WMDM_REVOKED</td>
<td>Windows Media Device Manager itself has been revoked.</td>
</tr>
<tr>
<td>WMDM_APP_REVOKED</td>
<td>The application has been revoked and needs to be updated before any DRM-protected content can be transferred.</td>
</tr>
<tr>
<td>WMDM_SP_REVOKED</td>
<td>The service provider has been revoked and needs to be updated before any DRM-protected content can be transferred to it.</td>
</tr>
<tr>
<td>WMDM_SCP_REVOKED</td>
<td>The secured content provider has been revoked and needs to be updated before any DRM-protected content can be transferred.</td>
</tr>
</table>

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method retrieves the URL from which updated components can be downloaded. If this method is not implemented by the revoked component, a default Microsoft URL is used. This location is maintained by Microsoft and contains any updates to components revoked by the Microsoft digital rights management system.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmrevoked">IWMDMRevoked Interface</a>
