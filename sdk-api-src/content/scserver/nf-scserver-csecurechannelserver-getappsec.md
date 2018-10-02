---
UID: NF:scserver.CSecureChannelServer.GetAppSec
title: CSecureChannelServer::GetAppSec
author: windows-sdk-content
description: The GetAppSec method retrieves the application security levels of the local and remote components. This method is published and available, but normally is used only by Windows Media Device Manager.
old-location: wmdm\csecurechannelserver_getappsec.htm
tech.root: WMDM
ms.assetid: 60659c36-ef9a-46fd-9a61-4a5a5210fd1f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],GetAppSec method, CSecureChannelServer.GetAppSec, CSecureChannelServer::GetAppSec, CSecureChannelServerGetAppSec, GetAppSec, GetAppSec method [windows Media Device Manager], GetAppSec method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::GetAppSec, wmdm.csecurechannelserver_getappsec
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
 - CSecureChannelServer.GetAppSec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CSecureChannelServer::GetAppSec


## -description



The <b>GetAppSec</b> method retrieves the application security levels of the local and remote components. This method is published and available, but normally is used only by Windows Media Device Manager.




## -parameters




### -param pdwLocalAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the local component.


### -param pdwRemoteAppSec [out]

Pointer to a <b>DWORD</b> specifying the application security level of the remote component.


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
 




## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>
 

 

