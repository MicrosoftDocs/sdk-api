---
UID: NF:netfw.NetworkIsolationRegisterForAppContainerChanges
title: NetworkIsolationRegisterForAppContainerChanges function (netfw.h)
description: The NetworkIsolationRegisterForAppContainerChanges function is used to register for the delivery of notifications regarding changes to an app container. 
helpviewer_keywords: ["INET_FIREWALL_AC_BINARY","INET_FIREWALL_AC_MAX","INET_FIREWALL_AC_NONE","INET_FIREWALL_AC_PACKAGE_ID_ONLY","NetworkIsolationRegisterForAppContainerChanges","NetworkIsolationRegisterForAppContainerChanges function [ICS/ICF]","ics.networkisolationregisterforappcontainerchanges","networkisolation/NetworkIsolationRegisterForAppContainerChanges"]
old-location: ics\networkisolationregisterforappcontainerchanges.htm
tech.root: ics
ms.assetid: 2affb2a8-224c-4d2d-86e2-f194d3990dbe
ms.date: 08/02/2022
ms.keywords: INET_FIREWALL_AC_BINARY, INET_FIREWALL_AC_MAX, INET_FIREWALL_AC_NONE, INET_FIREWALL_AC_PACKAGE_ID_ONLY, NetworkIsolationRegisterForAppContainerChanges, NetworkIsolationRegisterForAppContainerChanges function [ICS/ICF], ics.networkisolationregisterforappcontainerchanges, networkisolation/NetworkIsolationRegisterForAppContainerChanges
req.header: netfw.h
req.include-header: Netfw.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Firewallapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationRegisterForAppContainerChanges
 - netfw/NetworkIsolationRegisterForAppContainerChanges
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
 - API-MS-Win-Net-Isolation-l1-1-0.dll
 - API-MS-Win-Net-Isolation-l1-1-1.dll
 - wfapihost.dll
api_name:
 - NetworkIsolationRegisterForAppContainerChanges
---

# NetworkIsolationRegisterForAppContainerChanges function


## -description

The <b>NetworkIsolationRegisterForAppContainerChanges</b> function is used to register for the delivery of notifications regarding changes to an app container.

## -parameters

### -param flags [in]

Type: <b>DWORD</b>

A bitmask value of control flags which specify when to receive notifications. May contain one or more of the following flags. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_NONE"></a><a id="inet_firewall_ac_none"></a><dl>
<dt><b>INET_FIREWALL_AC_NONE</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
No notifications will be delivered.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_PACKAGE_ID_ONLY_"></a><a id="inet_firewall_ac_package_id_only_"></a><dl>
<dt><b>INET_FIREWALL_AC_PACKAGE_ID_ONLY </b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Notifications will be delivered when an app container is created with a package identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_BINARY"></a><a id="inet_firewall_ac_binary"></a><dl>
<dt><b>INET_FIREWALL_AC_BINARY</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Notifications will be delivered when  an app container is created with a binary path.

</td>
</tr>
<tr>
<td width="40%"><a id="INET_FIREWALL_AC_MAX"></a><a id="inet_firewall_ac_max"></a><dl>
<dt><b>INET_FIREWALL_AC_MAX</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Maximum value for testing purposes.

</td>
</tr>
</table>

### -param callback [in]

Type: <b><a href="/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn">PAC_CHANGES_CALLBACK_FN</a></b>

Function pointer that will be invoked when a notification is ready for delivery.

### -param context [in, optional]

Type: <b>PVOID</b>

Optional context pointer. This pointer is passed to the <i>callback</i> function along with details of the change.

### -param registrationObject [out]

Type: <b>HANDLE*</b>

Handle to the newly created registration.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationunregisterforappcontainerchanges">NetworkIsolationUnregisterForAppContainerChanges</a>



<a href="/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn">PAC_CHANGES_CALLBACK_FN</a>
