---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.OnVirtualMachineHostStatusChanged
title: ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of the host of a virtual machine is changed.
helpviewer_keywords: ["ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services]","OnVirtualMachineHostStatusChanged method","ITsSbProvisioningPluginNotifySink.OnVirtualMachineHostStatusChanged","ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged","OnVirtualMachineHostStatusChanged","OnVirtualMachineHostStatusChanged method [Remote Desktop Services]","OnVirtualMachineHostStatusChanged method [Remote Desktop Services]","ITsSbProvisioningPluginNotifySink interface","sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged","termserv.itssbprovisioningpluginnotifysink_onvirtualmachinehoststatuschanged"]
old-location: termserv\itssbprovisioningpluginnotifysink_onvirtualmachinehoststatuschanged.htm
tech.root: TermServ
ms.assetid: d86e9092-42ca-4e62-8613-cdcf2f8b627d
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],OnVirtualMachineHostStatusChanged method, ITsSbProvisioningPluginNotifySink.OnVirtualMachineHostStatusChanged, ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged, OnVirtualMachineHostStatusChanged, OnVirtualMachineHostStatusChanged method [Remote Desktop Services], OnVirtualMachineHostStatusChanged method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged, termserv.itssbprovisioningpluginnotifysink_onvirtualmachinehoststatuschanged
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
 - ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged
 - sbtsv/ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged
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
 - ITsSbProvisioningPluginNotifySink.OnVirtualMachineHostStatusChanged
---

# ITsSbProvisioningPluginNotifySink::OnVirtualMachineHostStatusChanged


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the status of the host of a virtual machine is changed.

## -parameters

### -param VmHost [in]

The name of the host.

### -param VmHostNotifyStatus [in]

The new status of the host.

### -param ErrorCode [in]

A standard <b>HRESULT</b> error code describing the reason for the status change.

### -param ErrorDescr [in]

A text description of the reason for the change.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a>