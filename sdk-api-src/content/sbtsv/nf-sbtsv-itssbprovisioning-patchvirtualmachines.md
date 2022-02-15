---
UID: NF:sbtsv.ITsSbProvisioning.PatchVirtualMachines
title: ITsSbProvisioning::PatchVirtualMachines (sbtsv.h)
description: Patches a virtual machine asynchronously.
helpviewer_keywords: ["ITsSbProvisioning interface [Remote Desktop Services]","PatchVirtualMachines method","ITsSbProvisioning.PatchVirtualMachines","ITsSbProvisioning::PatchVirtualMachines","PatchVirtualMachines","PatchVirtualMachines method [Remote Desktop Services]","PatchVirtualMachines method [Remote Desktop Services]","ITsSbProvisioning interface","sbtsv/ITsSbProvisioning::PatchVirtualMachines","termserv.itssbprovisioning_patchvirtualmachines"]
old-location: termserv\itssbprovisioning_patchvirtualmachines.htm
tech.root: TermServ
ms.assetid: 99afcba2-5567-47fa-9752-80394f145176
ms.date: 12/05/2018
ms.keywords: ITsSbProvisioning interface [Remote Desktop Services],PatchVirtualMachines method, ITsSbProvisioning.PatchVirtualMachines, ITsSbProvisioning::PatchVirtualMachines, PatchVirtualMachines, PatchVirtualMachines method [Remote Desktop Services], PatchVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, sbtsv/ITsSbProvisioning::PatchVirtualMachines, termserv.itssbprovisioning_patchvirtualmachines
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
 - ITsSbProvisioning::PatchVirtualMachines
 - sbtsv/ITsSbProvisioning::PatchVirtualMachines
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
 - ITsSbProvisioning.PatchVirtualMachines
---

# ITsSbProvisioning::PatchVirtualMachines


## -description

Patches a virtual machine asynchronously.

## -parameters

### -param JobXmlString [in]

Defines the job.

### -param JobGuid [in]

A <b>GUID</b> that identifies the job.

### -param pSink [in]

The <a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a> object that notifies the RD Connection Broker about the job.

### -param pVMPatchInfo [in, optional]

Patch information.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>