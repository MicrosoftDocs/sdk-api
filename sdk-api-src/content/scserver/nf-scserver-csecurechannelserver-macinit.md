---
UID: NF:scserver.CSecureChannelServer.MACInit
title: CSecureChannelServer::MACInit method
author: windows-driver-content
description: The MACInit method acquires a message authentication code (MAC) channel for use in calls to the MACUpdate and MACFinal methods.
old-location: wmdm\csecurechannelserver_macinit.htm
old-project: WMDM
ms.assetid: 92161bf3-8e2f-4b4a-a09a-98e33637df27
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: CSecureChannelServer, CSecureChannelServer interface [windows Media Device Manager], MACInit method, CSecureChannelServer::MACInit, CSecureChannelServerMACInit, MACInit method [windows Media Device Manager], MACInit method [windows Media Device Manager], CSecureChannelServer interface, MACInit,CSecureChannelServer.MACInit, scserver/CSecureChannelServer::MACInit, wmdm.csecurechannelserver_macinit
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
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mssachlp.lib
-	mssachlp.dll
api_name:
-	CSecureChannelServer.MACInit
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# CSecureChannelServer::MACInit method


## -description



The <b>MACInit</b> method acquires a message authentication code (MAC) channel for use in calls to the <b>MACUpdate</b> and <b>MACFinal</b> methods.




## -parameters




### -param phMAC [out]

Pointer to a MAC handle.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

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
<td>The phMAC parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



The <b>MACInit</b> method begins a message authentication code (MAC) session. This method must be called every time a (MAC) is required. <b>MACUpdate</b> and <b>MACFinal</b> must be called sequentially after <b>MACInit</b>. After <b>MACFinal</b>, <b>MACInit</b> must be called again to acquire a new handle.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
g_pAppSCServer = new CsecureChannelServer();
if( dwRead )
{
    // MAC the parameters.
    HMAC hMAC;
    
    g_pAppSCServer-&gt;MACInit(&amp;hMAC);
    g_pAppSCServer-&gt;MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead);
    g_pAppSCServer-&gt;MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD));
    g_pAppSCServer-&gt;MACFinal(hMAC, abMac);
    
    g_pAppSCServer-&gt;EncryptParam(pTmpData, dwRead);
    
    memcpy(pData, pTmpData, dwRead);
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>



<a href="https://msdn.microsoft.com/047340a5-5382-443e-a6d5-ecbcdfe9a210">CSecureChannelServer::MACFinal</a>



<a href="https://msdn.microsoft.com/f8b5548d-ffd5-4dc3-8d08-61a65841a997">CSecureChannelServer::MACUpdate</a>



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

