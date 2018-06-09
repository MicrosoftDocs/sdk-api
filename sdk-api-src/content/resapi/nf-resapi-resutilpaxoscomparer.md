---
UID: NF:resapi.ResUtilPaxosComparer
title: ResUtilPaxosComparer function
author: windows-sdk-content
description: Compares two Paxos tags and indicates whether they have the same values.
old-location: mscs\resutilpaxoscomparer.htm
old-project: MsCS
ms.assetid: 414F9BB0-2490-43A9-BE38-877B283573E1
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ResUtilPaxosComparer, ResUtilPaxosComparer function [Failover Cluster], mscs.resutilpaxoscomparer, resapi/ResUtilPaxosComparer
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
 - ResUtilPaxosComparer
product: Windows
targetos: Windows
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ResUtilPaxosComparer function


## -description


Compares two Paxos tags and indicates whether they have the same values.


## -parameters




### -param left [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the first Paxos tag to use in the comparison.


### -param right [in]

The <a href="https://msdn.microsoft.com/732CB125-F43A-4CC4-BC3F-EFB511BB7F2E">PaxosTagCStruct</a> structure that represents the second  Paxos tag to use in the comparison.


## -returns



<b>TRUE</b> if the Paxos tags have the same values; otherwise <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

