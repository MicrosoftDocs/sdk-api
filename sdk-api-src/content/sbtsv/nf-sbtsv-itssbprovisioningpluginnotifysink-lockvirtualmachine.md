---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.LockVirtualMachine
title: ITsSbProvisioningPluginNotifySink::LockVirtualMachine (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the virtual machine is locked.
helpviewer_keywords: ["ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services]","LockVirtualMachine method","ITsSbProvisioningPluginNotifySink.LockVirtualMachine","ITsSbProvisioningPluginNotifySink::LockVirtualMachine","LockVirtualMachine","LockVirtualMachine method [Remote Desktop Services]","LockVirtualMachine method [Remote Desktop Services]","ITsSbProvisioningPluginNotifySink interface","sbtsv/ITsSbProvisioningPluginNotifySink::LockVirtualMachine","termserv.itssbprovisioningpluginnotifysink_lockvirtualmachine"]
old-location: termserv\itssbprovisioningpluginnotifysink_lockvirtualmachine.htm
tech.root: TermServ
ms.assetid: 48eeaf06-3c6e-4c45-b5cd-9301dce7caee
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],LockVirtualMachine method, ITsSbProvisioningPluginNotifySink.LockVirtualMachine, ITsSbProvisioningPluginNotifySink::LockVirtualMachine, LockVirtualMachine, LockVirtualMachine method [Remote Desktop Services], LockVirtualMachine method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::LockVirtualMachine, termserv.itssbprovisioningpluginnotifysink_lockvirtualmachine
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
 - ITsSbProvisioningPluginNotifySink::LockVirtualMachine
 - sbtsv/ITsSbProvisioningPluginNotifySink::LockVirtualMachine
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
 - ITsSbProvisioningPluginNotifySink.LockVirtualMachine
---

# ITsSbProvisioningPluginNotifySink::LockVirtualMachine


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the virtual machine is locked.

## -parameters

### -param pVmNotifyEntry [in]

Notification entry.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a>