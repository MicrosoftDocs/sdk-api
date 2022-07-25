---
UID: NF:sbtsv.ITsSbProvisioning.CreateVirtualMachines
title: ITsSbProvisioning::CreateVirtualMachines (sbtsv.h)
description: Creates a virtual machine asynchronously.
helpviewer_keywords: ["CreateVirtualMachines","CreateVirtualMachines method [Remote Desktop Services]","CreateVirtualMachines method [Remote Desktop Services]","ITsSbProvisioning interface","ITsSbProvisioning interface [Remote Desktop Services]","CreateVirtualMachines method","ITsSbProvisioning.CreateVirtualMachines","ITsSbProvisioning::CreateVirtualMachines","sbtsv/ITsSbProvisioning::CreateVirtualMachines","termserv.itssbprovisioning_createvirtualmachines"]
old-location: termserv\itssbprovisioning_createvirtualmachines.htm
tech.root: TermServ
ms.assetid: 752da6d8-d036-4a39-aed5-c1fd7a11474e
ms.date: 12/05/2018
ms.keywords: CreateVirtualMachines, CreateVirtualMachines method [Remote Desktop Services], CreateVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, ITsSbProvisioning interface [Remote Desktop Services],CreateVirtualMachines method, ITsSbProvisioning.CreateVirtualMachines, ITsSbProvisioning::CreateVirtualMachines, sbtsv/ITsSbProvisioning::CreateVirtualMachines, termserv.itssbprovisioning_createvirtualmachines
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
 - ITsSbProvisioning::CreateVirtualMachines
 - sbtsv/ITsSbProvisioning::CreateVirtualMachines
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
 - ITsSbProvisioning.CreateVirtualMachines
---

# ITsSbProvisioning::CreateVirtualMachines


## -description

Creates a virtual machine asynchronously.

## -parameters

### -param JobXmlString [in]

Defines the job.

### -param JobGuid [in]

A <b>GUID</b> that identifies the job.

### -param pSink [in]

The <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a> object that notifies the RD Connection Broker about the job.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbprovisioning-canceljob">CancelJob</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>