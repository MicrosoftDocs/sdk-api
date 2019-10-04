---
UID: NN:comadmin.ICOMAdminCatalog2
title: ICOMAdminCatalog2 (comadmin.h)
author: windows-sdk-content
description: An extension of the ICOMAdminCatalog interface.
old-location: cos\icomadmincatalog2.htm
tech.root: cossdk
ms.assetid: ffca611d-dacc-47be-9101-9de76ecc8393
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICOMAdminCatalog2, ICOMAdminCatalog2 interface [COM+], ICOMAdminCatalog2 interface [COM+],described, comadmin/ICOMAdminCatalog2, cos.icomadmincatalog2
ms.topic: interface
f1_keywords: 
 - "comadmin/ICOMAdminCatalog2"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICOMAdminCatalog2 interface


## -description


An extension of the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nn-comadmin-icomadmincatalog">ICOMAdminCatalog</a> interface. The <b>ICOMAdminCatalog2</b> methods are used to control the interactions of applications, components, and partitions. These methods enable developers to control application execution, to dump applications or partitions to disk, to move components between applications, and to move applications between partitions.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog2</b> interface inherits from <b>ICOMAdminCatalog</b>. <b>ICOMAdminCatalog2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
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
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-aliascomponent">AliasComponent</a>
</td>
<td align="left" width="63%">
Creates an alias for an existing COM+ component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-areapplicationinstancespaused">AreApplicationInstancesPaused</a>
</td>
<td align="left" width="63%">
Determines whether any of the specified application instances (processes) are paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-copyapplications">CopyApplications</a>
</td>
<td align="left" width="63%">
Copies the specified COM+ applications from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-copycomponents">CopyComponents</a>
</td>
<td align="left" width="63%">
Copies the specified components from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-createserviceforapplication">CreateServiceForApplication</a>
</td>
<td align="left" width="63%">
Configures  a COM+ application to run as a Windows service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-deleteserviceforapplication">DeleteServiceForApplication</a>
</td>
<td align="left" width="63%">
Deletes the Windows service associated with the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-dumpapplicationinstance">DumpApplicationInstance</a>
</td>
<td align="left" width="63%">
Creates a dump file containing an image of the state of the specified application instance (process).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-exportpartition">ExportPartition</a>
</td>
<td align="left" width="63%">
Exports a partition to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-flushpartitioncache">FlushPartitionCache</a>
</td>
<td align="left" width="63%">
Empties the cache that maps users to their default partitions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getapplicationinstanceidfromprocessid">GetApplicationInstanceIDFromProcessID</a>
</td>
<td align="left" width="63%">
Retrieives the application instance identifier for the specified process identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcollectionbyquery2">GetCollectionByQuery2</a>
</td>
<td align="left" width="63%">
Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getcomponentversioncount">GetComponentVersionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of partitions in which a specified component is installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getpartitionid">GetPartitionID</a>
</td>
<td align="left" width="63%">
Retrieves  the partition identifier for the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-getpartitionname">GetPartitionName</a>
</td>
<td align="left" width="63%">
Retrieves  the name of the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-importcomponents">ImportComponents</a>
</td>
<td align="left" width="63%">
Imports the specified components that are already registered into an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-importunconfiguredcomponents">ImportUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Imports the specified classes into a COM+ application as unconfigured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-installpartition">InstallPartition</a>
</td>
<td align="left" width="63%">
Imports a partition from a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-issafetodelete">IsSafeToDelete</a>
</td>
<td align="left" width="63%">
Determines whether the specified DLL is in use by the COM+ catalog or the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-movecomponents">MoveComponents</a>
</td>
<td align="left" width="63%">
Moves the specified components from one application to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-pauseapplicationinstances">PauseApplicationInstances</a>
</td>
<td align="left" width="63%">
Pauses the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-promoteunconfiguredcomponents">PromoteUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Promotes the specified classes from unconfigured components to configured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-queryapplicationfile2">QueryApplicationFile2</a>
</td>
<td align="left" width="63%">
Retrieves information about an application that is about to be installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-recycleapplicationinstances">RecycleApplicationInstances</a>
</td>
<td align="left" width="63%">
Recycles (shuts down and restarts) the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-resumeapplicationinstances">ResumeApplicationInstances</a>
</td>
<td align="left" width="63%">
Resumes the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-shutdownapplicationinstances">ShutdownApplicationInstances</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-put_currentpartition">CurrentPartition</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-get_currentpartitionid">CurrentPartitionID</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-get_currentpartitionname">CurrentPartitionName</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-get_globalpartitionid">GlobalPartitionID</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-get_is64bitcatalogserver">Is64BitCatalogServer</a>


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

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icomadmincatalog2-get_isapplicationinstancedumpsupported">IsApplicationInstanceDumpSupported</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the software required for application instance dumps is installed.

</td>
</tr>
</table> 

