---
UID: NF:scserver.CSecureChannelServer.SetSessionKey
title: CSecureChannelServer::SetSessionKey
author: windows-driver-content
description: The SetSessionKey method sets the session key that is used to communicate with another component. This method is published and available, but normally is used only by Windows Media Device Manager.
old-location: wmdm\csecurechannelserver_setsessionkey.htm
old-project: WMDM
ms.assetid: 207435a6-0b16-49d9-a366-878331732a14
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],SetSessionKey method, CSecureChannelServer.SetSessionKey, CSecureChannelServer::SetSessionKey, CSecureChannelServerSetSessionKey, SetSessionKey, SetSessionKey method [windows Media Device Manager], SetSessionKey method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::SetSessionKey, wmdm.csecurechannelserver_setsessionkey
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
-	CSecureChannelServer.SetSessionKey
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CSecureChannelServer::SetSessionKey


## -description



The <b>SetSessionKey</b> method sets the session key that is used to communicate with another component. This method is published and available, but normally is used only by Windows Media Device Manager.




## -parameters




### -param pbSPSessionKey [in]

Pointer to the first byte of the session key that is to be set. The key is used for encryption and decryption.


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



<a href="https://msdn.microsoft.com/1be09669-434e-4774-92bf-4ea470d6c4b9">CSecureChannelServer::GetSessionKey</a>
 

 

