---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
<th>
                  Flag
                </th>
<th>
                  Description
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
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method retrieves the URL from which updated components can be downloaded. If this method is not implemented by the revoked component, a default Microsoft URL is used. This location is maintained by Microsoft and contains any updates to components revoked by the Microsoft digital rights management system.




## -see-also




<a href="https://msdn.microsoft.com/b627f243-3652-4db9-8a5e-6a2146b73424">IWMDMRevoked Interface</a>
 

 

