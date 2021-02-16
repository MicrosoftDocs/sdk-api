---
UID: NF:tssbx.IWTSSBPlugin.WTSSBX_MachineChangeNotification
title: IWTSSBPlugin::WTSSBX_MachineChangeNotification (tssbx.h)
description: Notifies the plug-in that a change occurred in the server environment.
helpviewer_keywords: ["IWTSSBPlugin interface [Remote Desktop Services]","WTSSBX_MachineChangeNotification method","IWTSSBPlugin.WTSSBX_MachineChangeNotification","IWTSSBPlugin::WTSSBX_MachineChangeNotification","WTSSBX_MachineChangeNotification","WTSSBX_MachineChangeNotification method [Remote Desktop Services]","WTSSBX_MachineChangeNotification method [Remote Desktop Services]","IWTSSBPlugin interface","termserv.iwtssbplugin_wtssbx_machinechangenotification","tssbx/IWTSSBPlugin::WTSSBX_MachineChangeNotification"]
old-location: termserv\iwtssbplugin_wtssbx_machinechangenotification.htm
tech.root: TermServ
ms.assetid: 226ca68e-6c3d-4160-a569-ca0b92cb9316
ms.date: 12/05/2018
ms.keywords: IWTSSBPlugin interface [Remote Desktop Services],WTSSBX_MachineChangeNotification method, IWTSSBPlugin.WTSSBX_MachineChangeNotification, IWTSSBPlugin::WTSSBX_MachineChangeNotification, WTSSBX_MachineChangeNotification, WTSSBX_MachineChangeNotification method [Remote Desktop Services], WTSSBX_MachineChangeNotification method [Remote Desktop Services],IWTSSBPlugin interface, termserv.iwtssbplugin_wtssbx_machinechangenotification, tssbx/IWTSSBPlugin::WTSSBX_MachineChangeNotification
req.header: tssbx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tssbx.idl
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
 - IWTSSBPlugin::WTSSBX_MachineChangeNotification
 - tssbx/IWTSSBPlugin::WTSSBX_MachineChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tssbx.h
api_name:
 - IWTSSBPlugin.WTSSBX_MachineChangeNotification
---

# IWTSSBPlugin::WTSSBX_MachineChangeNotification


## -description

<p class="CCE_Message">[The <a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a> interface is 
    not supported  after Windows Server 2008 R2. Starting with Windows Server 2012 please use the 
    <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a> interface.]

Notifies the plug-in that a change occurred in the server environment.

## -parameters

### -param NotificationType [in]

A value of the <a href="/windows/win32/api/tssbx/ne-tssbx-wtssbx_notification_type">WTSSBX_NOTIFICATION_TYPE</a> enumeration type that indicates the type of event that occurred.

### -param MachineId [in]

The ID of the server on which the change  occurred.

### -param pMachineInfo [in]

A pointer to a <a href="/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info">WTSSBX_MACHINE_INFO</a> structure that contains information about the server that changed. Only the members that changed are reported in this structure. The other members are set to zero.

## -returns

Returns <b>S_OK</b> if successful.

## -remarks

Terminal Services Session Broker (TS Session Broker) calls this method whenever an important change in the server environment occurs. For example, changes that would trigger a call include when:

<ul>
<li>A server joins or leaves a farm in TS Session Broker.</li>
<li>A server changes its drain state.</li>
<li>A server IP address changes.</li>
<li>A server's maximum session limit changes.</li>
</ul>
Your implementation of this method must return <b>S_OK</b> immediately if successful.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin">ITsSbPlugin</a>



<a href="/windows/desktop/api/tssbx/nn-tssbx-iwtssbplugin">IWTSSBPlugin</a>