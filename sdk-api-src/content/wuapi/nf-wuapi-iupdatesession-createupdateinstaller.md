---
UID: NF:wuapi.IUpdateSession.CreateUpdateInstaller
title: IUpdateSession::CreateUpdateInstaller (wuapi.h)
description: Returns an IUpdateInstaller interface for this session.
helpviewer_keywords: ["CreateUpdateInstaller","CreateUpdateInstaller method [Windows Update Agent]","CreateUpdateInstaller method [Windows Update Agent]","IUpdateSession interface","IUpdateSession interface [Windows Update Agent]","CreateUpdateInstaller method","IUpdateSession.CreateUpdateInstaller","IUpdateSession::CreateUpdateInstaller","wua.iupdatesession_createupdateinstaller","wuapi/IUpdateSession::CreateUpdateInstaller"]
old-location: wua\iupdatesession_createupdateinstaller.htm
tech.root: wua
ms.assetid: e5b5f760-0d25-4506-95d3-63ff4a0b9188
ms.date: 12/05/2018
ms.keywords: CreateUpdateInstaller, CreateUpdateInstaller method [Windows Update Agent], CreateUpdateInstaller method [Windows Update Agent],IUpdateSession interface, IUpdateSession interface [Windows Update Agent],CreateUpdateInstaller method, IUpdateSession.CreateUpdateInstaller, IUpdateSession::CreateUpdateInstaller, wua.iupdatesession_createupdateinstaller, wuapi/IUpdateSession::CreateUpdateInstaller
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSession::CreateUpdateInstaller
 - wuapi/IUpdateSession::CreateUpdateInstaller
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSession.CreateUpdateInstaller
---

# IUpdateSession::CreateUpdateInstaller


## -description

Returns an <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> interface for this session.

## -parameters

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> interface for this session.

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

An <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateinstaller">IUpdateInstaller</a> interface can also be created by using the UpdateInstaller coclass.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesession">IUpdateSession</a>