---
UID: NF:msclus.ISClusResDependencies.AddItem
title: ISClusResDependencies::AddItem
author: windows-sdk-content
description: Adds an existing cluster resource to the dependency collection.
old-location: mscs\clusresdependencies_additem.htm
old-project: MsCS
ms.assetid: f8462df8-dece-423f-a585-5774411401c8
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: AddItem, AddItem method [Failover Cluster], AddItem method [Failover Cluster],ClusResDependencies class, ClusResDependencies class [Failover Cluster],AddItem method, ClusResDependencies.AddItem, ISClusResDependencies.AddItem, ISClusResDependencies::AddItem, _wolf_clusresdependencies.additem, mscs.clusresdependencies_additem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ClusResDependencies.AddItem
 - ISClusResDependencies.AddItem
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusResDependencies::AddItem


## -description


<p class="CCE_Message">[The <b>AddItem</b> 
    method is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Adds an 
    existing cluster <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a> to the 
    <a href="https://msdn.microsoft.com/en-us/library/aa369367(v=vs.85).aspx">dependency</a> collection.


## -parameters




### -param pResource






#### - objResource

The <a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a> object to add to the 
      collection.


## -returns



This method does not return a value.




## -remarks



Resources added to a 
    <a href="https://msdn.microsoft.com/10695840-38ec-4614-8bbd-5772a53dea4b">ClusResDependencies</a> collection become 
    <a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependencies</a> of the resource from which the 
    collection was obtained


#### Examples

The following script uses the <b>AddItem</b> 
     method to add a dependency to a resource.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''
' adddependency.vbs
' Adds a dependency to a resource. Both resources must already exist
' and be able to form a dependency relationship. Run the script on 
' the command line using the following syntax:
'     AddDependency Resourcename Dependencyname
' The resource identified by Resourcename will depend on the resource
' identified by Dependencyname.
'''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''''' 
Option Explicit
Dim objArgs, objCluster, objResource, objDependency
Set objArgs = WScript.Arguments
If objArgs.Count &lt;&gt; 2 Then
    WScript.Echo "Syntax:   AddDependency Resourcename Dependencyname"
    WScript.Quit
End If
Set objCluster = CreateObject("MSCluster.Cluster")
objClus.Open ""
Set objResource = objCluster.Resources.Item(objArgs(0))
Set objDependency = objCluster.Resources.Item(objArgs(1))
If objResource.CanResourceBeDependent(objDependency) Then
    objResource.Dependencies.AddItem(objDependency)
Else
    WScript.Echo objResource.Name &amp; " cannot depend on " &amp; objDependency.Name
End If
Set objResource = Nothing
Set objDependency = Nothing
Set objCluster = Nothing
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/10695840-38ec-4614-8bbd-5772a53dea4b">ClusResDependencies</a>



<a href="https://msdn.microsoft.com/c1b66495-c428-4ee4-94e2-263fd31f61ad">ClusResource</a>
 

 

