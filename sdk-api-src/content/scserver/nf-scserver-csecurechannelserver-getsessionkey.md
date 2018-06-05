---
UID: NF:scserver.CSecureChannelServer.GetSessionKey
title: CSecureChannelServer::GetSessionKey
author: windows-sdk-content
description: The GetSessionKey method retrieves the current session key that is used for encryption and decryption. This method is published and available, but normally is used only by Windows Media Device Manager.
old-location: wmdm\csecurechannelserver_getsessionkey.htm
old-project: WMDM
ms.assetid: 1be09669-434e-4774-92bf-4ea470d6c4b9
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],GetSessionKey method, CSecureChannelServer.GetSessionKey, CSecureChannelServer::GetSessionKey, CSecureChannelServerGetSessionKey, GetSessionKey, GetSessionKey method [windows Media Device Manager], GetSessionKey method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::GetSessionKey, wmdm.csecurechannelserver_getsessionkey
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	CSecureChannelServer.GetSessionKey
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CSecureChannelServer::GetSessionKey


## -description



The <b>GetSessionKey</b> method retrieves the current session key that is used for encryption and decryption. This method is published and available, but normally is used only by Windows Media Device Manager.




## -parameters




### -param pbSPSessionKey [out]

Pointer to the first byte of a buffer containing the session key.


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
<td>The pbSPSessionKey parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>



<a href="https://msdn.microsoft.com/207435a6-0b16-49d9-a366-878331732a14">CSecureChannelServer::SetSessionKey</a>
 

 

