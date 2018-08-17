---
UID: NF:msclus.ISClusNode.Resume
title: ISClusNode::Resume
author: windows-sdk-content
description: Resumes the cluster activity of a node after it has been paused by the ClusNode.Pause method.
old-location: mscs\clusnode_resume.htm
old-project: mscs
ms.assetid: 74e465e2-1328-4e05-b287-3ce27359c67a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ClusNode object [Failover Cluster],Resume method, ClusNode.Resume, ISClusNode.Resume, ISClusNode::Resume, Resume, Resume method [Failover Cluster], Resume method [Failover Cluster],ClusNode object, _wolf_clusnode.resume, mscs.clusnode_resume
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msclus.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsClus.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsClus.tlb
tech.root: 
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsClus.dll
api_name:
 - ClusNode.Resume
 - ISClusNode.Resume
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusNode::Resume


## -description


<p class="CCE_Message">[The <b>Resume</b> method is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Resumes the 
    <a href="c_gly.htm">cluster</a> activity of a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a> after it has been 
    <a href="p_gly.htm">paused</a> by the 
    <a href="https://msdn.microsoft.com/2fd16dda-b554-47fa-a040-15c7685d6392">ClusNode.Pause</a> method.


## -parameters






## -returns



This method does not return a value.




## -remarks



When a node resumes cluster activity after it has been paused, it returns 
    <b>ClusterNodeUp</b> as the value for its 
    <a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">ClusNode.State</a> property.




## -see-also




<a href="https://msdn.microsoft.com/b164f5a6-13f1-4eff-a2f9-805b60138dd1">ClusNode</a>



<a href="https://msdn.microsoft.com/2fd16dda-b554-47fa-a040-15c7685d6392">ClusNode.Pause</a>



<a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">ClusNode.State</a>
 

 

