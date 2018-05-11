---
UID: NN:msclus.ISCluster
title: ISCluster
author: windows-driver-content
description: Enables operations on the cluster and provides access to all of the objects in the cluster.
old-location: mscs\cluster_object.htm
old-project: MsCS
ms.assetid: 4a765dce-c823-4a79-8608-ff41feec8a39
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Cluster, Cluster object [Failover Cluster], Cluster object [Failover Cluster],described, ISCluster, _wolf_cluster_object, msclus/Cluster, mscs.cluster_object
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
-	Cluster
-	ISCluster
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISCluster interface


## -description


<p class="CCE_Message">[The <b>Cluster</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Enables operations on the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> and provides access to all of the objects in the 
    cluster.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Cluster</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>Cluster</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a connection to a cluster.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Cluster</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/99de61b9-2979-404a-bbed-94d6f5eea2da">CommonProperties</a>


</td>
<td align="left" width="63%">
Returns the read/write <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a> of the 
     cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fcd27e3b-4895-445f-a578-f08ccd110a99">CommonROProperties</a>


</td>
<td align="left" width="63%">
Returns the read-only common properties of the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Returns the current name of a cluster or allows a new name to be assigned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f4fbac67-f196-4fd8-a678-8f7877e70f6a">NetInterfaces</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/7d0dc4fd-733c-4a2a-9136-7dc0089b213d">ClusNetInterfaces</a> 
     collection providing access to the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> 
     in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/352f186d-bf42-480a-9554-c764345dafe6">Networks</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/7dba0985-16bc-4bda-9f37-275032c07811">ClusNetworks</a> collection 
     providing access to the <a href="https://msdn.microsoft.com/57d16e1f-e774-4ffb-b26b-7e72d6d589aa">networks</a> in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/690c9635-114f-4109-a9b9-4ebb1961c58b">Nodes</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/f35d610f-014a-48cf-aaa4-93e320bcd890">ClusNodes</a> collection providing 
     access to the <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">nodes</a> in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f866a25f-64ef-4289-b95a-c55cb90a5d42">PrivateProperties</a>


</td>
<td align="left" width="63%">
Returns the read-only private properties of the cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6a89c7ea-4f53-46c5-8373-ffbaf0a7a8cd">PrivateROProperties</a>


</td>
<td align="left" width="63%">
Returns the read/write <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a> of the 
     cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/38dff875-1fb9-4173-9d47-a9a9643770fe">QuorumLogSize</a>


</td>
<td align="left" width="63%">
Sets or returns the maximum size of the log file maintained by the quorum resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5f1c6a47-5f28-40b7-9b36-551335ac72d4">QuorumPath</a>


</td>
<td align="left" width="63%">
Sets or returns the path to the log file maintained by the 
     <a href="https://msdn.microsoft.com/4c2ee30e-4de2-44ba-93ba-d2d89196545e">quorum resource</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e9c1f32a-2008-470e-b451-312cce49c93a">QuorumResource</a>


</td>
<td align="left" width="63%">
Specifies or returns a <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object 
     representing the current quorum resource for a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/449e4432-571c-403c-81c7-da50f455224c">ResourceGroups</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a> collection 
     providing access to the <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/fdfdd1de-fa4a-4bfb-80e1-15b2141d488b">Resources</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/56dd53e7-7e2e-481f-b343-da51c7c52553">ClusResources</a> collection 
     providing access to the <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a> in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/73a9ca85-0da2-4978-965a-47bdee4ded6c">ResourceTypes</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/614d3ed6-255f-46ed-9354-7a73a21cac87">ClusResTypes</a> collection 
     providing access to the <a href="https://msdn.microsoft.com/d02e4f51-7b86-451a-a51c-ea850ae464d1">resource types</a> in a cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn973197">Version</a>


</td>
<td align="left" width="63%">
Returns a <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> object describing the 
     <a href="c_gly.htm">cluster version</a>.

</td>
</tr>
</table> 


## -remarks



<b>Cluster</b> is a top-level object, allowing new object 
    instances to be created. For example:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim objCluster as Cluster
Set objCluster = New Cluster
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

