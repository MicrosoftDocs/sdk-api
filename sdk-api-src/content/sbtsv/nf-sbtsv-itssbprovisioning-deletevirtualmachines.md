---
UID: NF:sbtsv.ITsSbProvisioning.DeleteVirtualMachines
title: ITsSbProvisioning::DeleteVirtualMachines (sbtsv.h)
author: windows-sdk-content
description: Deletes a virtual machine asynchronously.
old-location: termserv\itssbprovisioning_deletevirtualmachines.htm
tech.root: TermServ
ms.assetid: 45f5398d-2d27-4f6b-9020-bcbb44edc89a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteVirtualMachines, DeleteVirtualMachines method [Remote Desktop Services], DeleteVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, ITsSbProvisioning interface [Remote Desktop Services],DeleteVirtualMachines method, ITsSbProvisioning.DeleteVirtualMachines, ITsSbProvisioning::DeleteVirtualMachines, sbtsv/ITsSbProvisioning::DeleteVirtualMachines, termserv.itssbprovisioning_deletevirtualmachines
ms.topic: method
f1_keywords: ["sbtsv/ITsSbProvisioning.DeleteVirtualMachines"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvisioning.DeleteVirtualMachines
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The <a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink">ITsSbProvisioningPluginNotifySink</a> object that notifies the RD Connection Broker about the job.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning">ITsSbProvisioning</a>
 

 

