---
UID: NF:sbtsv.ITsSbProvisioningPluginNotifySink.OnJobCompleted
title: ITsSbProvisioningPluginNotifySink::OnJobCompleted
author: windows-driver-content
description: Notifies Remote Desktop Connection Broker (RD Connection Broker) that the job is complete.
old-location: termserv\itssbprovisioningpluginnotifysink_onjobcompleted.htm
old-project: TermServ
ms.assetid: 7d0399c8-2161-4d6e-8c14-7fd5bc2757b8
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ITsSbProvisioningPluginNotifySink interface [Remote Desktop Services],OnJobCompleted method, ITsSbProvisioningPluginNotifySink.OnJobCompleted, ITsSbProvisioningPluginNotifySink::OnJobCompleted, OnJobCompleted, OnJobCompleted method [Remote Desktop Services], OnJobCompleted method [Remote Desktop Services],ITsSbProvisioningPluginNotifySink interface, sbtsv/ITsSbProvisioningPluginNotifySink::OnJobCompleted, termserv.itssbprovisioningpluginnotifysink_onjobcompleted
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
-	ITsSbProvisioningPluginNotifySink.OnJobCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6f91021c-d7a5-4131-bef7-b4f5f37f9f8b">ITsSbProvisioningPluginNotifySink</a>
 

 

