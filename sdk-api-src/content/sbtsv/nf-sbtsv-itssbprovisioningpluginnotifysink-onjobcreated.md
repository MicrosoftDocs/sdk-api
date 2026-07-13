---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.OnJobCreated
title: ITsSbProvisioningPluginNotifySink::OnJobCreated (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that a provisioning job is created.
helpviewer_keywords: ["ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services]","OnJobCreated method","ITsSbProvisioningPluginNotifySink.OnJobCreated","ITsSbProvisioningPluginNotifySink::OnJobCreated","OnJobCreated","OnJobCreated method [Remote Desktop Services]","OnJobCreated method [Remote Desktop Services]","ITsSbProvisioningPluginNotifySink interface","sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCreated","termserv.itssbprovisioningpluginnotifysink_onjobcreated"]
old-location: termserv\itssbprovisioningpluginnotifysink_onjobcreated.htm
tech.root: TermServ
ms.assetid: daab9172-d984-4b47-9f64-59216513aff7
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],OnJobCreated method, ITsSbProvisioningPluginNotifySink.OnJobCreated, ITsSbProvisioningPluginNotifySink::OnJobCreated, OnJobCreated, OnJobCreated method [Remote Desktop Services], OnJobCreated method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCreated, termserv.itssbprovisioningpluginnotifysink_onjobcreated
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
 - ITsSbProvisioningPluginNotifySink::OnJobCreated
 - sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCreated
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
 - ITsSbProvisioningPluginNotifySink.OnJobCreated
---

# ITsSbProvisioningPluginNotifySink::OnJobCreated


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that a provisioning job is created.

## -parameters

### -param pVmNotifyInfo [in]

Notification info.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a>