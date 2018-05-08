---
UID: NN:msclus.ISClusApplication
title: ISClusApplication
author: windows-driver-content
description: Provides access to the DomainNames and ClusterNames collections and opens a connection to a specified cluster.
old-location: mscs\clusapplication_object.htm
old-project: MsCS
ms.assetid: 2f837658-18f5-44c9-b743-1980a616e71a
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: ClusApplication, ClusApplication object [Failover Cluster], ClusApplication object [Failover Cluster],described, ISClusApplication, _wolf_clusapplication_object, msclus/ClusApplication, mscs.clusapplication_object
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: msclus.h
req.include-header: 
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
req.typenames: CLUS_GROUP_START_SETTING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	MsClus.dll
api_name:
-	ClusApplication
-	ISClusApplication
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusApplication interface


## -description


<p class="CCE_Message">[The <b>ClusApplication</b> 
    object is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

The <b>ClusApplication</b> object provides 
    access to the <a href="https://msdn.microsoft.com/e7f806a7-02e7-41be-b8b9-60351180e748">DomainNames</a> and 
    <a href="https://msdn.microsoft.com/c4e29498-c4e2-4351-8eed-05bc73437485">ClusterNames</a> collections and opens a 
    connection to a specified <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusApplication</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ClusApplication</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2501e921-5b0a-429f-aa7f-56191ab9795b">OpenCluster</a>
</td>
<td align="left" width="63%">
Opens a connection to a cluster.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusApplication</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5c4d64e1-d8cb-4abb-b157-3ecdf02a6219">ClusterNames</a>


</td>
<td align="left" width="63%">
Returns the names of all the clusters in a domain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/418274eb-a366-4df8-af84-7e4ba8eeed5f">DomainNames</a>


</td>
<td align="left" width="63%">
Returns the names of all available domains.

</td>
</tr>
</table> 


## -remarks



<b>ClusApplication</b> is a top-level object, 
    allowing new object instances to be created.


#### Examples

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim objApplication as ClusApplication
Set objApplication = New ClusApplication
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/37d11232-ef16-46c3-a914-1c0d358eca1a">Application Management Objects</a>
 

 

