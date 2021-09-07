---
UID: NF:sbtsv.ITsSbProvisioning.DeleteVirtualMachines
title: ITsSbProvisioning::DeleteVirtualMachines (sbtsv.h)
description: Deletes a virtual machine asynchronously.
helpviewer_keywords: ["DeleteVirtualMachines","DeleteVirtualMachines method [Remote Desktop Services]","DeleteVirtualMachines method [Remote Desktop Services]","ITsSbProvisioning interface","ITsSbProvisioning interface [Remote Desktop Services]","DeleteVirtualMachines method","ITsSbProvisioning.DeleteVirtualMachines","ITsSbProvisioning::DeleteVirtualMachines","sbtsv/ITsSbProvisioning::DeleteVirtualMachines","termserv.itssbprovisioning_deletevirtualmachines"]
old-location: termserv\itssbprovisioning_deletevirtualmachines.htm
tech.root: TermServ
ms.assetid: 45f5398d-2d27-4f6b-9020-bcbb44edc89a
ms.date: 12/05/2018
ms.keywords: DeleteVirtualMachines, DeleteVirtualMachines method [Remote Desktop Services], DeleteVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, ITsSbProvisioning interface [Remote Desktop Services],DeleteVirtualMachines method, ITsSbProvisioning.DeleteVirtualMachines, ITsSbProvisioning::DeleteVirtualMachines, sbtsv/ITsSbProvisioning::DeleteVirtualMachines, termserv.itssbprovisioning_deletevirtualmachines
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
 - ITsSbProvisioning::DeleteVirtualMachines
 - sbtsv/ITsSbProvisioning::DeleteVirtualMachines
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
 - ITsSbProvisioning.DeleteVirtualMachines
---

# ITsSbProvisioning::DeleteVirtualMachines


## -description

Deletes a virtual machine asynchronously.

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

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>