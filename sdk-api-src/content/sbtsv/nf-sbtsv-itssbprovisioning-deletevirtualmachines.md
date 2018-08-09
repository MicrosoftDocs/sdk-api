---
UID: NF:sbtsv.ITsSbProvisioning.DeleteVirtualMachines
title: ITsSbProvisioning::DeleteVirtualMachines
author: windows-sdk-content
description: Deletes a virtual machine asynchronously.
old-location: termserv\itssbprovisioning_deletevirtualmachines.htm
old-project: termserv
ms.assetid: 45f5398d-2d27-4f6b-9020-bcbb44edc89a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeleteVirtualMachines, DeleteVirtualMachines method [Remote Desktop Services], DeleteVirtualMachines method [Remote Desktop Services],ITsSbProvisioning interface, ITsSbProvisioning interface [Remote Desktop Services],DeleteVirtualMachines method, ITsSbProvisioning.DeleteVirtualMachines, ITsSbProvisioning::DeleteVirtualMachines, sbtsv/ITsSbProvisioning::DeleteVirtualMachines, termserv.itssbprovisioning_deletevirtualmachines
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
 - ITsSbProvisioning.DeleteVirtualMachines
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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

The <a href="https://msdn.microsoft.com/6f91021c-d7a5-4131-bef7-b4f5f37f9f8b">ITsSbProvisioningPluginNotifySink</a> object that notifies the RD Connection Broker about the job.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/136c1538-be4f-4b1c-b74f-8914a51f774a">ITsSbProvisioning</a>
 

 

