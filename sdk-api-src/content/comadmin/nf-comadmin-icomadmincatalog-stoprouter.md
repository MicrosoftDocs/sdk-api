---
UID: NF:comadmin.ICOMAdminCatalog.StopRouter
title: ICOMAdminCatalog::StopRouter (comadmin.h)
description: Stops the component load balancing service if the service is currently installed.
helpviewer_keywords: ["ICOMAdminCatalog interface [COM+]","StopRouter method","ICOMAdminCatalog.StopRouter","ICOMAdminCatalog::StopRouter","StopRouter","StopRouter method [COM+]","StopRouter method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_StopRouter","comadmin/ICOMAdminCatalog::StopRouter","cos.icomadmincatalog_stoprouter"]
old-location: cos\icomadmincatalog_stoprouter.htm
tech.root: cos
ms.assetid: 23b0e4af-bdab-4f58-b3ab-82aab5516b48
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog interface [COM+],StopRouter method, ICOMAdminCatalog.StopRouter, ICOMAdminCatalog::StopRouter, StopRouter, StopRouter method [COM+], StopRouter method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_StopRouter, comadmin/ICOMAdminCatalog::StopRouter, cos.icomadmincatalog_stoprouter
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICOMAdminCatalog::StopRouter
 - comadmin/ICOMAdminCatalog::StopRouter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog.StopRouter
---

# ICOMAdminCatalog::StopRouter


## -description

Stops the component load balancing service if the service is currently installed.



## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and E_FAIL, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_SERVICENOTINSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The component load balancing service is not currently installed on the computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMADMIN_E_OBJECTERRORS</b></dt>
</dl>
</td>
<td width="60%">
Errors occurred while accessing one or more objects.

</td>
</tr>
</table>

## -remarks

When called on a computer acting as the component load balancing (CLB) server, the <b>StopRouter</b> method stops the server from routing component activation requests to other servers in the application cluster.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>
