---
UID: NF:wuapi.IUpdateSession.CreateUpdateInstaller
title: IUpdateSession::CreateUpdateInstaller
author: windows-sdk-content
description: Returns an IUpdateInstaller interface for this session.
old-location: wua\iupdatesession_createupdateinstaller.htm
old-project: wua_sdk
ms.assetid: e5b5f760-0d25-4506-95d3-63ff4a0b9188
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CreateUpdateInstaller, CreateUpdateInstaller method [Windows Update Agent], CreateUpdateInstaller method [Windows Update Agent],IUpdateSession interface, IUpdateSession interface [Windows Update Agent],CreateUpdateInstaller method, IUpdateSession.CreateUpdateInstaller, IUpdateSession::CreateUpdateInstaller, wua.iupdatesession_createupdateinstaller, wuapi/IUpdateSession::CreateUpdateInstaller
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSession.CreateUpdateInstaller
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSession::CreateUpdateInstaller


## -description


Returns an <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface for this session.


## -parameters




### -param retval [out]

An <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface for this session.


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



An <a href="https://msdn.microsoft.com/7f1c272f-73ef-43ee-b1ac-ef97a4791313">IUpdateInstaller</a> interface can also be created by using the UpdateInstaller coclass.




## -see-also




<a href="https://msdn.microsoft.com/00b84246-b5f2-48c2-a0ab-eaaa1ec80262">IUpdateSession</a>
 

 

