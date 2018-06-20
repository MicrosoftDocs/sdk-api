---
UID: NF:msclus.ISClusVersion.get_MajorVersion
title: ISClusVersion::get_MajorVersion
author: windows-sdk-content
description: Returns the integer portion of the version number for the operating system installed on the local node.
old-location: mscs\clusversion_majorversion.htm
old-project: MsCS
ms.assetid: f4d81e0a-4f65-470b-9215-f1b91e582646
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ClusVersion object [Failover Cluster],MajorVersion property, ClusVersion.MajorVersion, ISClusVersion.get_MajorVersion, ISClusVersion::get_MajorVersion, MajorVersion property [Failover Cluster], MajorVersion property [Failover Cluster],ClusVersion object, _wolf_clusversion.majorversion, get_MajorVersion, mscs.clusversion_majorversion
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
 - ClusVersion.MajorVersion
 - ISClusVersion.get_MajorVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion::get_MajorVersion


## -description


<p class="CCE_Message">[The <b>MajorVersion</b> 
    property is available for use in the operating systems specified in the Requirements section. It may be altered or 
    unavailable in subsequent versions.]

Returns the 
    integer portion of the version number for the operating system  installed on the local 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>.

This property is read-only.


## -parameters


## -remarks



The <b>MajorVersion</b> and 
    <a href="https://msdn.microsoft.com/c335922c-ac62-4b37-bafb-b29d58545c85">ClusVersion.MinorVersion</a> properties together 
    form a complete Windows <a href="https://msdn.microsoft.com/en-us/library/aa373122(v=vs.85).aspx">version number</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Version = X.Y
MajorVersion = X
MinorVersion = Y
</pre>
</td>
</tr>
</table></span></div>
All <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> properties are static values 
    corresponding the state of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> when the 
    <b>ClusVersion</b> object was first created. To obtain the 
    latest version information from the cluster, create a new 
    <b>ClusVersion</b> object.


#### Examples

See <a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a> for an 
     example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2215335a-1858-437f-8654-2e9d601fe061">ClusVersion</a>



<a href="https://msdn.microsoft.com/a7f32e65-98d6-4d69-a796-c0b4bcfe8316">ClusVersion.CSDVersion</a>



<a href="https://msdn.microsoft.com/c335922c-ac62-4b37-bafb-b29d58545c85">ClusVersion.MinorVersion</a>
 

 

