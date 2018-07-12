---
UID: NC:resapi.PQUORUM_RESOURCE_LOST
title: PQUORUM_RESOURCE_LOST
author: windows-sdk-content
description: Called when control of the quorum resource has been lost.
old-location: mscs\quorumresourcelost.htm
old-project: mscs
ms.assetid: 353eaf47-f93e-4243-8bed-7b6f07513a3c
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: PQUORUM_RESOURCE_LOST, PQUORUM_RESOURCE_LOST callback function [Failover Cluster], QuorumResourceLost, QuorumResourceLost callback, QuorumResourceLost callback function [Failover Cluster], _wolf_quorumresourcelost, mscs.quorumresourcelost, resapi/PQUORUM_RESOURCE_LOST, resapi/QuorumResourceLost
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ResApi.h
api_name:
 - QuorumResourceLost
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PQUORUM_RESOURCE_LOST callback function


## -description


Called when control of the <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a> has 
    been lost. The <b>PQUORUM_RESOURCE_LOST</b> type defines a pointer to this 
    function.


## -parameters




### -param Resource








#### - ResourceHandle [in]

Handle identifying the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> to which this callback 
       applies. The value for <i>ResourceHandle</i> should be the handle passed in during the 
       <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> call for this resource.


## -returns



This function has no return values.




## -remarks



The <i>QuorumResourceLost</i> callback function is 
     called by a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a> to notify the 
     <a href="https://msdn.microsoft.com/caebb47f-c2c5-463e-a957-d9eefc7fc33d">Resource Monitor</a> that control of the quorum resource has 
     been lost after arbitration. A pointer to the Resource Monitor's 
     <i>QuorumResourceLost</i> callback function is passed to 
     a quorum resource DLL in the call to <a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>.




## -see-also




<a href="https://msdn.microsoft.com/dc16b785-bbb1-4917-a826-e49445a86c26">Arbitrate</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>



<a href="https://msdn.microsoft.com/6c7de7e6-a0f5-4308-8cf3-21968bd339a4">Resource DLL Callback Functions</a>
 

 

