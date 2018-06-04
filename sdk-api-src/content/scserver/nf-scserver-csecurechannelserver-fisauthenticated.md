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

# CSecureChannelServer::fIsAuthenticated


## -description



The <b>fIsAuthenticated</b> method verifies that a <a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Secure Authenticated Channel</a> has been successfully established.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method is used to ensure that a secure authenticated channel has been established between components before allowing certain operations. This includes calls by devices and storages prior to accessing and transferring data streams. You should confirm that this method returns <b>TRUE</b> before calling other top-level methods on the component.

Applications do not need to call the <b>fIsAuthenticated</b> method, but service providers do. They should call this method for all exposed APIs and return WMDM_E_NOTCERTIFIED if it returns <b>FALSE</b>.


#### Examples

The following code shows a service provider's implementation of <a href="https://msdn.microsoft.com/88c935ad-dbf0-41bb-8676-ddafe9d1fe0e">IMDSPDevice::GetVersion</a>. This method verifies that a secure authenticated channel has been established before returning the version.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT CMyDevice::GetVersion(DWORD * pdwVersion)
{
    HRESULT hr
 = S_OK;
    
    if(g_pAppSCServer == NULL)
        return E_FAIL;

    if (!(g_pAppSCServer-&gt;fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    *pdwVersion = 1;
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9b9a529a-c652-48e1-b70d-e95e2e34e2c5">CSecureChannelClient::fIsAuthenticated</a>



<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>
 

 

