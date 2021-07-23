---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.OnJobCompleted
title: ITsSbProvisioningPluginNotifySink::OnJobCompleted (sbtsv.h)
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the job is complete.
helpviewer_keywords: ["ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services]","OnJobCompleted method","ITsSbProvisioningPluginNotifySink.OnJobCompleted","ITsSbProvisioningPluginNotifySink::OnJobCompleted","OnJobCompleted","OnJobCompleted method [Remote Desktop Services]","OnJobCompleted method [Remote Desktop Services]","ITsSbProvisioningPluginNotifySink interface","sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCompleted","termserv.itssbprovisioningpluginnotifysink_onjobcompleted"]
old-location: termserv\itssbprovisioningpluginnotifysink_onjobcompleted.htm
tech.root: TermServ
ms.assetid: 7d0399c8-2161-4d6e-8c14-7fd5bc2757b8
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],OnJobCompleted method, ITsSbProvisioningPluginNotifySink.OnJobCompleted, ITsSbProvisioningPluginNotifySink::OnJobCompleted, OnJobCompleted, OnJobCompleted method [Remote Desktop Services], OnJobCompleted method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCompleted, termserv.itssbprovisioningpluginnotifysink_onjobcompleted
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
 - ITsSbProvisioningPluginNotifySink::OnJobCompleted
 - sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCompleted
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
 - ITsSbProvisioningPluginNotifySink.OnJobCompleted
---

# ITsSbProvisioningPluginNotifySink::OnJobCompleted


## -description

Notifies Remote Desktop Connection Broker (RD Connection Broker) that the job is complete.

## -parameters

### -param ResultCode [in]

The <b>HRESULT</b> returned by the job.

### -param ResultDescription [in]

A text description of the <i>ResultCode</i>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a>