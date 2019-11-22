---
UID: NF:wuapi.IUpdateSession.CreateUpdateSearcher
title: IUpdateSession::CreateUpdateSearcher (wuapi.h)

description: Returns an IUpdateSearcher interface for this session.
old-location: wua\iupdatesession_createupdatesearcher.htm
tech.root: Wua_Sdk
ms.assetid: 7e7a4aa9-7952-4080-9ac0-9544f959475f

ms.date: 12/05/2018
ms.keywords: CreateUpdateSearcher, CreateUpdateSearcher method [Windows Update Agent], CreateUpdateSearcher method [Windows Update Agent],IUpdateSession interface, IUpdateSession interface [Windows Update Agent],CreateUpdateSearcher method, IUpdateSession.CreateUpdateSearcher, IUpdateSession::CreateUpdateSearcher, wua.iupdatesession_createupdatesearcher, wuapi/IUpdateSession::CreateUpdateSearcher
ms.topic: method
f1_keywords: 
 - "wuapi/IUpdateSession.CreateUpdateSearcher"
dev_langs:
 - c++
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
 - IUpdateSession.CreateUpdateSearcher
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateSession::CreateUpdateSearcher


## -description


Returns an <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface for this session.


## -parameters




### -param retval [out]

An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface for this session.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, a COM or Windows error code. 

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
</table>
 




## -remarks



An <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> interface can also be created by using the UpdateSearcher coclass.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesession">IUpdateSession</a>
 

 

