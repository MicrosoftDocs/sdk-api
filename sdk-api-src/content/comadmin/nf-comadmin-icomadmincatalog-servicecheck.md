---
UID: NF:comadmin.ICOMAdminCatalog.ServiceCheck
title: ICOMAdminCatalog::ServiceCheck (comadmin.h)
description: Retrieves the current status of the specified COM+ service.
helpviewer_keywords: ["COMAdminServiceContinuePending","COMAdminServicePausePending","COMAdminServicePaused","COMAdminServiceRunning","COMAdminServiceStartPending","COMAdminServiceStopPending","COMAdminServiceStopped","COMAdminServiceUnknownState","ICOMAdminCatalog interface [COM+]","ServiceCheck method","ICOMAdminCatalog.ServiceCheck","ICOMAdminCatalog::ServiceCheck","ServiceCheck","ServiceCheck method [COM+]","ServiceCheck method [COM+]","ICOMAdminCatalog interface","_cos_ICOMAdminCatalog_ServiceCheck","comadmin/ICOMAdminCatalog::ServiceCheck","cos.icomadmincatalog_servicecheck"]
old-location: cos\icomadmincatalog_servicecheck.htm
tech.root: cos
ms.assetid: d7d41691-30ab-450c-b93b-b7b02f408eb1
ms.date: 12/05/2018
ms.keywords: COMAdminServiceContinuePending, COMAdminServicePausePending, COMAdminServicePaused, COMAdminServiceRunning, COMAdminServiceStartPending, COMAdminServiceStopPending, COMAdminServiceStopped, COMAdminServiceUnknownState, ICOMAdminCatalog interface [COM+],ServiceCheck method, ICOMAdminCatalog.ServiceCheck, ICOMAdminCatalog::ServiceCheck, ServiceCheck, ServiceCheck method [COM+], ServiceCheck method [COM+],ICOMAdminCatalog interface, _cos_ICOMAdminCatalog_ServiceCheck, comadmin/ICOMAdminCatalog::ServiceCheck, cos.icomadmincatalog_servicecheck
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
 - ICOMAdminCatalog::ServiceCheck
 - comadmin/ICOMAdminCatalog::ServiceCheck
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
 - ICOMAdminCatalog.ServiceCheck
---

# ICOMAdminCatalog::ServiceCheck


## -description

Retrieves the current status of the specified COM+ service.

## -parameters

### -param lService [in]

The service for which status is to be checked. This parameter can be COMAdminServiceLoadBalanceRouter
(1) to check the component load balancing service.

### -param plStatus [out, retval]

The status for the specified service.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceStopped"></a><a id="comadminservicestopped"></a><a id="COMADMINSERVICESTOPPED"></a><dl>
<dt><b>COMAdminServiceStopped</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The service is stopped.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceStartPending"></a><a id="comadminservicestartpending"></a><a id="COMADMINSERVICESTARTPENDING"></a><dl>
<dt><b>COMAdminServiceStartPending</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The service is due to start.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceStopPending"></a><a id="comadminservicestoppending"></a><a id="COMADMINSERVICESTOPPENDING"></a><dl>
<dt><b>COMAdminServiceStopPending</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The service is due to stop.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceRunning"></a><a id="comadminservicerunning"></a><a id="COMADMINSERVICERUNNING"></a><dl>
<dt><b>COMAdminServiceRunning</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The service is running.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceContinuePending"></a><a id="comadminservicecontinuepending"></a><a id="COMADMINSERVICECONTINUEPENDING"></a><dl>
<dt><b>COMAdminServiceContinuePending</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The service is due to continue.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServicePausePending"></a><a id="comadminservicepausepending"></a><a id="COMADMINSERVICEPAUSEPENDING"></a><dl>
<dt><b>COMAdminServicePausePending</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The service is due to pause.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServicePaused"></a><a id="comadminservicepaused"></a><a id="COMADMINSERVICEPAUSED"></a><dl>
<dt><b>COMAdminServicePaused</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The service is paused.

</td>
</tr>
<tr>
<td width="40%"><a id="COMAdminServiceUnknownState"></a><a id="comadminserviceunknownstate"></a><a id="COMADMINSERVICEUNKNOWNSTATE"></a><dl>
<dt><b>COMAdminServiceUnknownState</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
The service status is unknown.

</td>
</tr>
</table>

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a>