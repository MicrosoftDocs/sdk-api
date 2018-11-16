---
UID: NF:wuapi.IUpdateSession.CreateUpdateDownloader
title: IUpdateSession::CreateUpdateDownloader
author: windows-sdk-content
description: Returns an IUpdateDownloader interface for this session.
old-location: wua\iupdatesession_createupdatedownloader.htm
tech.root: Wua_Sdk
ms.assetid: 9d410114-2327-489c-84b6-c3f5367008c2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateUpdateDownloader, CreateUpdateDownloader method [Windows Update Agent], CreateUpdateDownloader method [Windows Update Agent],IUpdateSession interface, IUpdateSession interface [Windows Update Agent],CreateUpdateDownloader method, IUpdateSession.CreateUpdateDownloader, IUpdateSession::CreateUpdateDownloader, wua.iupdatesession_createupdatedownloader, wuapi/IUpdateSession::CreateUpdateDownloader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSession.CreateUpdateDownloader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wuapi.h
: 
- IUpdateSession.CreateUpdateDownloader
: 
---

# IUpdateSession::CreateUpdateDownloader


## -description


Returns an <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface for this session.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface for this session.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
</table>
 




## -remarks



An <a href="https://msdn.microsoft.com/8f9f3430-fc78-46cb-9dc8-b97e9d35d91c">IUpdateDownloader</a> interface can also be created by using the UpdateDownloader coclass.




## -see-also




<a href="https://msdn.microsoft.com/00b84246-b5f2-48c2-a0ab-eaaa1ec80262">IUpdateSession</a>
 

 

