---
UID: NF:traffic.TcQueryInterface
title: TcQueryInterface function (traffic.h)
description: The TcQueryInterface function queries traffic control for related per-interface parameters.
helpviewer_keywords: ["TcQueryInterface","TcQueryInterface function [QOS]","_gqos_tcqueryinterface","qos.tcqueryinterface","traffic/TcQueryInterface"]
old-location: qos\tcqueryinterface.htm
tech.root: QOS
ms.assetid: 7cbee5e9-fecc-4bfc-8b65-f3fc3427c85d
ms.date: 12/05/2018
ms.keywords: TcQueryInterface, TcQueryInterface function [QOS], _gqos_tcqueryinterface, qos.tcqueryinterface, traffic/TcQueryInterface
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TcQueryInterface
 - traffic/TcQueryInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcQueryInterface
---

# TcQueryInterface function


## -description

The 
<b>TcQueryInterface</b> function queries traffic control for related per-interface parameters. A traffic control parameter is queried by providing its globally unique identifier (GUID). Setting the <i>NotifyChange</i> parameter to <b>TRUE</b> enables event notification on the specified GUID, after which notification events are sent to a client whenever the queried parameter changes. GUIDs for which clients can request notification are found in the 
<a href="/previous-versions/windows/desktop/qos/guid">GUID</a> entry; the column titled "Notification" denotes which GUIDs are available for notification.

## -parameters

### -param IfcHandle [in]

Handle associated with the interface to be queried. This handle is obtained by a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a> function.

### -param pGuidParam [in]

Pointer to the globally unique identifier (GUID) that corresponds to the traffic control parameter being queried.

### -param NotifyChange [in]

Used to request notifications from traffic control for the parameter being queried. If <b>TRUE</b>, traffic control will notify the client, through the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a> function, upon changes to the parameter corresponding to the GUID provided in <i>pGuidParam</i>. Notifications are off by default.

### -param pBufferSize [in, out]

Indicates the size of the buffer, in bytes. For input, this value is the size of the buffer allocated by the caller. For output, this value is the actual size of the buffer, in bytes, used by traffic control.

### -param Buffer [out]

Pointer to a client-allocated buffer into which returned data will be written.

## -returns

Note that, with regard to a requested notification state, only a return value of NO_ERROR will result in the application of the requested notification state. If a return value other than NO_ERROR is returned from a call to the 
<b>TcQueryInterface</b> function, the requested change in notification state will not be accepted.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Invalid interface handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid or <b>NULL</b> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to store the results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Querying for the GUID provided is not supported on the provided interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The device did not register for this GUID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The instance name was not found, likely because the interface is in the process of being closed.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Use of the 
<b>TcQueryInterface</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateinterfaces">TcEnumerateInterfaces</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcregisterclient">TcRegisterClient</a>