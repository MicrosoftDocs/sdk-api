---
UID: NF:sbtsv.ITsSbProvisioning.CreateVirtualMachines
title: ITsSbProvisioning::CreateVirtualMachines method
author: windows-driver-content
description: Creates a virtual machine asynchronously.
old-location: termserv\itssbprovisioning_createvirtualmachines.htm
old-project: TermServ
ms.assetid: 752da6d8-d036-4a39-aed5-c1fd7a11474e
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreateVirtualMachines method [Remote Desktop Services], CreateVirtualMachines method [Remote Desktop Services], ITsSbProvisioning interface, CreateVirtualMachines,ITsSbProvisioning.CreateVirtualMachines, ITsSbProvisioning, ITsSbProvisioning interface [Remote Desktop Services], CreateVirtualMachines method, ITsSbProvisioning::CreateVirtualMachines, sbtsv/ITsSbProvisioning::CreateVirtualMachines, termserv.itssbprovisioning_createvirtualmachines
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TS_SB_SORT_BY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	sbtsv.h
api_name:
-	ITsSbProvisioning.CreateVirtualMachines
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# ITsSbProvisioning::CreateVirtualMachines method


## -description


Creates a virtual machine asynchronously.


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




<a href="https://msdn.microsoft.com/c0496a8c-00ec-43a4-a7c2-071acb6b068a">CancelJob</a>



<a href="https://msdn.microsoft.com/136c1538-be4f-4b1c-b74f-8914a51f774a">ITsSbProvisioning</a>
 

 

