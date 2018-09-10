---
UID: NN:comadmin.ICOMAdminCatalog2
title: ICOMAdminCatalog2
author: windows-sdk-content
description: An extension of the ICOMAdminCatalog interface.
old-location: cos\icomadmincatalog2.htm
tech.root: cossdk
ms.assetid: ffca611d-dacc-47be-9101-9de76ecc8393
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICOMAdminCatalog2, ICOMAdminCatalog2 interface [COM+], ICOMAdminCatalog2 interface [COM+],described, comadmin/ICOMAdminCatalog2, cos.icomadmincatalog2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICOMAdminCatalog2 interface


## -description


An extension of the <a href="https://msdn.microsoft.com/en-us/library/Ee309561(v=VS.85).aspx">ICOMAdminCatalog</a> interface. The <b>ICOMAdminCatalog2</b> methods are used to control the interactions of applications, components, and partitions. These methods enable developers to control application execution, to dump applications or partitions to disk, to move components between applications, and to move applications between partitions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog2</b> interface inherits from <b>ICOMAdminCatalog</b>. <b>ICOMAdminCatalog2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
</ul>

## -members

The <b>ICOMAdminCatalog2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684350(v=VS.85).aspx">AliasComponent</a>
</td>
<td align="left" width="63%">
Creates an alias for an existing COM+ component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686054(v=VS.85).aspx">AreApplicationInstancesPaused</a>
</td>
<td align="left" width="63%">
Determines whether any of the specified application instances (processes) are paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681256(v=VS.85).aspx">CopyApplications</a>
</td>
<td align="left" width="63%">
Copies the specified COM+ applications from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684240(v=VS.85).aspx">CopyComponents</a>
</td>
<td align="left" width="63%">
Copies the specified components from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685067(v=VS.85).aspx">CreateServiceForApplication</a>
</td>
<td align="left" width="63%">
Configures  a COM+ application to run as a Windows service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684138(v=VS.85).aspx">DeleteServiceForApplication</a>
</td>
<td align="left" width="63%">
Deletes the Windows service associated with the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682797(v=VS.85).aspx">DumpApplicationInstance</a>
</td>
<td align="left" width="63%">
Creates a dump file containing an image of the state of the specified application instance (process).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686479(v=VS.85).aspx">ExportPartition</a>
</td>
<td align="left" width="63%">
Exports a partition to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684134(v=VS.85).aspx">FlushPartitionCache</a>
</td>
<td align="left" width="63%">
Empties the cache that maps users to their default partitions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685077(v=VS.85).aspx">GetApplicationInstanceIDFromProcessID</a>
</td>
<td align="left" width="63%">
Retrieives the application instance identifier for the specified process identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685970(v=VS.85).aspx">GetCollectionByQuery2</a>
</td>
<td align="left" width="63%">
Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681724(v=VS.85).aspx">GetComponentVersionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of partitions in which a specified component is installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679167(v=VS.85).aspx">GetPartitionID</a>
</td>
<td align="left" width="63%">
Retrieves  the partition identifier for the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678904(v=VS.85).aspx">GetPartitionName</a>
</td>
<td align="left" width="63%">
Retrieves  the name of the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685169(v=VS.85).aspx">ImportComponents</a>
</td>
<td align="left" width="63%">
Imports the specified components that are already registered into an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681295(v=VS.85).aspx">ImportUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Imports the specified classes into a COM+ application as unconfigured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687112(v=VS.85).aspx">InstallPartition</a>
</td>
<td align="left" width="63%">
Imports a partition from a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679494(v=VS.85).aspx">IsSafeToDelete</a>
</td>
<td align="left" width="63%">
Determines whether the specified DLL is in use by the COM+ catalog or the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679901(v=VS.85).aspx">MoveComponents</a>
</td>
<td align="left" width="63%">
Moves the specified components from one application to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681711(v=VS.85).aspx">PauseApplicationInstances</a>
</td>
<td align="left" width="63%">
Pauses the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687606(v=VS.85).aspx">PromoteUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Promotes the specified classes from unconfigured components to configured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684129(v=VS.85).aspx">QueryApplicationFile2</a>
</td>
<td align="left" width="63%">
Retrieves information about an application that is about to be installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678926(v=VS.85).aspx">RecycleApplicationInstances</a>
</td>
<td align="left" width="63%">
Recycles (shuts down and restarts) the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681811(v=VS.85).aspx">ResumeApplicationInstances</a>
</td>
<td align="left" width="63%">
Resumes the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679233(v=VS.85).aspx">ShutdownApplicationInstances</a>
</td>
<td align="left" width="63%">
Initiates shutdown of the specified application server processes.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog2</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms679235(v=VS.85).aspx">CurrentPartition</a>


</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
The current destination partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686085(v=VS.85).aspx">CurrentPartitionID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The identifier for the current partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms681290(v=VS.85).aspx">CurrentPartitionName</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the current partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms685183(v=VS.85).aspx">GlobalPartitionID</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The identifier for the global partition.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms682270(v=VS.85).aspx">Is64BitCatalogServer</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the currently connected catalog server is a 64-bit computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686702(v=VS.85).aspx">IsApplicationInstanceDumpSupported</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the software required for application instance dumps is installed.

</td>
</tr>
</table> 

