---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.OnVirtualMachineStatusChanged
title: ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of a virtual machine is changed.
helpviewer_keywords: ["ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services]","OnVirtualMachineStatusChanged method","ITsSbProvisioningPluginNotifySink.OnVirtualMachineStatusChanged","ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged","OnVirtualMachineStatusChanged","OnVirtualMachineStatusChanged method [Remote Desktop Services]","OnVirtualMachineStatusChanged method [Remote Desktop Services]","ITsSbProvisioningPluginNotifySink interface","sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged","termserv.itssbprovisioningpluginnotifysink_onvirtualmachinestatuschanged"]
old-location: termserv\itssbprovisioningpluginnotifysink_onvirtualmachinestatuschanged.htm
tech.root: TermServ
ms.assetid: 5a256dec-fa40-48c2-b7e3-e89ec9e75f0e
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],OnVirtualMachineStatusChanged method, ITsSbProvisioningPluginNotifySink.OnVirtualMachineStatusChanged, ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged, OnVirtualMachineStatusChanged, OnVirtualMachineStatusChanged method [Remote Desktop Services], OnVirtualMachineStatusChanged method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged, termserv.itssbprovisioningpluginnotifysink_onvirtualmachinestatuschanged
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged
 - sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvisioningPluginNotifySink.OnVirtualMachineStatusChanged
---

# ITsSbProvisioningPluginNotifySink::OnVirtualMachineStatusChanged


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of a virtual machine is changed.

## -parameters

### -param pVmNotifyEntry [in]

Notification entry.

### -param VmNotifyStatus [in]

Notification status.

### -param ErrorCode [in]

A standard <b>HRESULT</b> error code describing the reason for the status change.

### -param ErrorDescr [in]

A text description of the reason for the change.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a>