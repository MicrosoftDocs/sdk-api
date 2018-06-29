---
UID: NF:sbtsv.ITsSbProvisioning.PatchVirtualMachines
title: ITsSbProvisioning::PatchVirtualMachines
author: windows-sdk-content
description: Patches a virtual machine asynchronously.
old-location: termserv\itssbprovisioning_patchvirtualmachines.htm
old-project: TermServ
ms.assetid: 99afcba2-5567-47fa-9752-80394f145176
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ITsSbProvisioning interface [Remote Desktop Services],PatchVirtualMachines method, ITsSbProvisioning.PatchVirtualMachines, ITsSbProvisioning::PatchVirtualMachines, PatchVirtualMachines, PatchVirtualMachines method [Remote Desktop Services], PatchVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, sbtsv/ITsSbProvisioning::PatchVirtualMachines, termserv.itssbprovisioning_patchvirtualmachines
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvisioning.PatchVirtualMachines
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

The <a href="https://msdn.microsoft.com/6f91021c-d7a5-4131-bef7-b4f5f37f9f8b">ITsSbProvisioningPluginNotifySink</a> object that notifies the RD Connection Broker about the job.


### -param pVMPatchInfo [in, optional]

Patch information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/136c1538-be4f-4b1c-b74f-8914a51f774a">ITsSbProvisioning</a>
 

 

