---
UID: NN:msclus.ISClusVersion
title: ISClusVersion
author: windows-sdk-content
description: Provides version information about the operating system and the Cluster service. For more information on cluster versions and version numbers, see Version Compatibility.
old-location: mscs\clusversion_object.htm
old-project: mscs
ms.assetid: 2215335a-1858-437f-8654-2e9d601fe061
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: ClusVersion, ClusVersion object [Failover Cluster], ClusVersion object [Failover Cluster],described, ISClusVersion, _wolf_clusversion_object, msclus/ClusVersion, mscs.clusversion_object
ms.prod: windows
ms.technology: windows-sdk
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
 - ClusVersion
 - ISClusVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: MsClus.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISClusVersion interface


## -description


<p class="CCE_Message">[The <b>ClusVersion</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Provides version information 
    about the operating system and the <a href="c_gly.htm">Cluster service</a>. 
    For more information on <a href="c_gly.htm">cluster versions</a> and 
    <a href="v_gly.htm">version numbers</a>, see 
    <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.


## -remarks



A <b>ClusVersion</b> collection:

<ul>
<li>Is obtained from <a href="https://msdn.microsoft.com/77abfb85-48fe-4b18-b79e-5641711f33d7">Cluster.Version</a>.</li>
</ul>
Some of the <b>ClusVersion</b> properties correspond to 
    dynamic values maintained internally by the cluster. A 
    <b>ClusVersion</b> object is instantiated with a snapshot of 
    those values and stores them statically. Therefore, the 
    <b>ClusVersion</b> property values represent the state of 
    the cluster when the object was first created. To obtain the latest version information from the cluster, create a 
    new <b>ClusVersion</b> object.

For more information about the versioning process see 
    <a href="https://msdn.microsoft.com/919345fa-cbaa-4d01-bd3c-9ca69cab5094">Version Compatibility</a>.


#### Examples

The following script instantiates and uses a 
     <b>ClusVersion</b> object.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>'---------------------------------------------------------------------
' ClusVersion.vbs
' Uses the ClusVersion object to display version information about
' the local cluster.
'---------------------------------------------------------------------
Option Explicit
Const LOW16 = 65535
Dim objClus, objVers
Dim strVersion, strOSVersion, strHighest, strLowest

' Connect to the local cluster and get a ClusVersion object.
Set objClus = CreateObject("MSCluster.Cluster")
objClus.Open ""
Set objVers = objClus.Version

' Format a string describing the current version
strOSVersion = CStr(objVers.MajorVersion) &amp; "." &amp; _
               CStr(objVers.MinorVersion) &amp; "." &amp; _
               CStr(objVers.BuildNumber)

' Format a string describing the highest compatible version.
' We must extract the upper and lower 16 bits of the 32-bit value.
strHighest = CStr(CLng(objVers.ClusterHighestVersion / (2 ^ 15))) &amp; _
             ".0." &amp; _
             CStr(CLng(objVers.ClusterHighestVersion And LOW16))

' Format a string describing the lowest compatible version.
' We must extract the upper and lower 16 bits of the 32-bit value.
strLowest = CStr(CLng(objVers.ClusterLowestVersion / (2 ^ 15))) &amp; _
            ".0." &amp; _
            CStr(CLng(objVers.ClusterLowestVersion And LOW16))

' Format and display the output string.
strVersion = objVers.Name &amp; vbCrLf &amp; _
             objVers.VendorID &amp; " version " &amp; _
             strOSVersion &amp; vbCrLf &amp; "Compatible with versions: " &amp; _
             strLowest &amp; " and " &amp; strHighest &amp; vbCrLf
WScript.Echo strVersion

Set objVers = Nothing
Set objClus = Nothing
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8d4397e1-f24f-47b0-9037-e5a045337049">Cluster Management Objects</a>
 

 

