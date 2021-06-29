---
UID: NF:wuapi.IUpdate.AcceptEula
title: IUpdate::AcceptEula (wuapi.h)
description: Accepts the Microsoft Software License Terms that are associated with Windows Update.
helpviewer_keywords: ["AcceptEula","AcceptEula method [Windows Update Agent]","AcceptEula method [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","AcceptEula method","IUpdate.AcceptEula","IUpdate::AcceptEula","wua.iupdate_accepteula","wuapi/IUpdate::AcceptEula"]
old-location: wua\iupdate_accepteula.htm
tech.root: wua
ms.assetid: b3a25994-eace-45ec-8e6b-40d69796f168
ms.date: 12/05/2018
ms.keywords: AcceptEula, AcceptEula method [Windows Update Agent], AcceptEula method [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],AcceptEula method, IUpdate.AcceptEula, IUpdate::AcceptEula, wua.iupdate_accepteula, wuapi/IUpdate::AcceptEula
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
 - IUpdate::AcceptEula
 - wuapi/IUpdate::AcceptEula
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
 - IUpdate.AcceptEula
---

# IUpdate::AcceptEula


## -description

Accepts the Microsoft Software License Terms that are associated with Windows Update. Administrators and power users can call this method.



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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

(This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is implementing the interface has been locked down.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_EULA_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The Microsoft Software License Terms for the update could not be located.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>
