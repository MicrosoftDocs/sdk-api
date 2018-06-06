---
UID: NF:resapi.ResUtilLeftPaxosIsLessThanRight
title: ResUtilLeftPaxosIsLessThanRight function
author: windows-sdk-content
description: Indicates whether a specified Paxos tag contains older cluster configuration information than another specified Paxos tag.
old-location: mscs\resutilleftpaxosislessthanright.htm
old-project: MsCS
ms.assetid: 01CBFC67-02D0-439D-BE4E-EA0A2448FDEE
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ResUtilLeftPaxosIsLessThanRight, ResUtilLeftPaxosIsLessThanRight function [Failover Cluster], mscs.resutilleftpaxosislessthanright, resapi/ResUtilLeftPaxosIsLessThanRight
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016
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
req.typenames: RESOURCE_EXIT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilLeftPaxosIsLessThanRight
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ResUtilLeftPaxosIsLessThanRight function


## -description


Indicates whether a specified Paxos tag contains older cluster configuration information than another specified Paxos tag.


## -parameters




### -param left [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the first Paxos tag to use in the comparison.


### -param right [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the 2nd  Paxos tag to use in the comparison.


## -returns



<b>TRUE</b> if the cluster configuration of the first Paxos tag is older than the that of the second Paxos tag; otherwise <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

