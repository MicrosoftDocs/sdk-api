---
UID: NN:comadmin.ICOMAdminCatalog2
title: ICOMAdminCatalog2
author: windows-sdk-content
description: An extension of the ICOMAdminCatalog interface.
old-location: cos\icomadmincatalog2.htm
old-project: cossdk
ms.assetid: ffca611d-dacc-47be-9101-9de76ecc8393
ms.author: windowssdkdev
ms.date: 05/16/2018
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
tech.root: 
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICOMAdminCatalog2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog2 interface


## -description


An extension of the <a href="https://msdn.microsoft.com/2c3c49df-9ca5-40ea-b45c-f4eca1004602">ICOMAdminCatalog</a> interface. The <b>ICOMAdminCatalog2</b> methods are used to control the interactions of applications, components, and partitions. These methods enable developers to control application execution, to dump applications or partitions to disk, to move components between applications, and to move applications between partitions.


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
<a href="https://msdn.microsoft.com/99d43ef5-f117-4307-aa44-f149b4986cda">AliasComponent</a>
</td>
<td align="left" width="63%">
Creates an alias for an existing COM+ component.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b526dc2e-107c-4936-95ac-2c0c91f5c09b">AreApplicationInstancesPaused</a>
</td>
<td align="left" width="63%">
Determines whether any of the specified application instances (processes) are paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ddb9cab-2e02-4b96-9216-d6cb064f8107">CopyApplications</a>
</td>
<td align="left" width="63%">
Copies the specified COM+ applications from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/931f4929-b99b-4c4f-8980-eaceacc0e7fa">CopyComponents</a>
</td>
<td align="left" width="63%">
Copies the specified components from one partition to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ffc7366-c47a-487e-b40c-bdcea5dbf052">CreateServiceForApplication</a>
</td>
<td align="left" width="63%">
Configures  a COM+ application to run as a Windows service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bc4a72e-79a1-4780-a143-1ba1ec66812b">DeleteServiceForApplication</a>
</td>
<td align="left" width="63%">
Deletes the Windows service associated with the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76c121c6-4ba6-49da-93dc-9094acb1994c">DumpApplicationInstance</a>
</td>
<td align="left" width="63%">
Creates a dump file containing an image of the state of the specified application instance (process).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc793025-e8d9-4dcb-a55d-81dec38d05b9">ExportPartition</a>
</td>
<td align="left" width="63%">
Exports a partition to a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b5f6619-fbff-417d-b80a-a38532227059">FlushPartitionCache</a>
</td>
<td align="left" width="63%">
Empties the cache that maps users to their default partitions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a09569af-11ec-406a-a51c-72b81b84fe41">GetApplicationInstanceIDFromProcessID</a>
</td>
<td align="left" width="63%">
Retrieives the application instance identifier for the specified process identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1861e8f-bb42-42b5-9435-6fa366f8284a">GetCollectionByQuery2</a>
</td>
<td align="left" width="63%">
Retrieves a collection of items in the COM+ catalog that satisfy the specified set of query keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bbae408-3dbe-4f8f-92db-9ea1b8abd9ce">GetComponentVersionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of partitions in which a specified component is installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12fa83e1-b2d2-48c3-a002-ac2f8043b54a">GetPartitionID</a>
</td>
<td align="left" width="63%">
Retrieves  the partition identifier for the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/08d3efb2-1e2e-42e3-aefe-644db3b480f4">GetPartitionName</a>
</td>
<td align="left" width="63%">
Retrieves  the name of the specified COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7ae28f9-6be6-4774-974a-a5d7f3ebbc02">ImportComponents</a>
</td>
<td align="left" width="63%">
Imports the specified components that are already registered into an application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51bab6c7-5ec2-4651-a0c4-c54683a65d75">ImportUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Imports the specified classes into a COM+ application as unconfigured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f54a6a-9b90-4e9e-b94c-46f6c9b683a3">InstallPartition</a>
</td>
<td align="left" width="63%">
Imports a partition from a file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/293644a2-e400-47fc-803d-cf86ba97eb7d">IsSafeToDelete</a>
</td>
<td align="left" width="63%">
Determines whether the specified DLL is in use by the COM+ catalog or the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38cc4726-4b61-4f4b-9719-161297361f45">MoveComponents</a>
</td>
<td align="left" width="63%">
Moves the specified components from one application to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59771a5d-894b-46de-9874-ece4aca7232f">PauseApplicationInstances</a>
</td>
<td align="left" width="63%">
Pauses the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6ed7fa7-3736-4e82-a153-116f4aa141a1">PromoteUnconfiguredComponents</a>
</td>
<td align="left" width="63%">
Promotes the specified classes from unconfigured components to configured components.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b2f9ce5-f2d8-4359-ac58-5069d6d58bb7">QueryApplicationFile2</a>
</td>
<td align="left" width="63%">
Retrieves information about an application that is about to be installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d2d6255-54c7-4110-9ee0-7019e9c7cb83">RecycleApplicationInstances</a>
</td>
<td align="left" width="63%">
Recycles (shuts down and restarts) the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/675ecabc-1414-4cf6-b691-805e9a5cb61c">ResumeApplicationInstances</a>
</td>
<td align="left" width="63%">
Resumes the specified application server processes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1de6c76b-f6f1-44d3-9bd4-4b6ac921893a">ShutdownApplicationInstances</a>
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

<a href="https://msdn.microsoft.com/1df71c0b-0abe-48c3-baa2-8c04b2aa171d">CurrentPartition</a>


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

<a href="https://msdn.microsoft.com/bba572c7-54c5-4c98-9d05-5f72d5648e6a">CurrentPartitionID</a>


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

<a href="https://msdn.microsoft.com/51254edf-420b-42a3-a3b8-a71c23a4cb49">CurrentPartitionName</a>


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

<a href="https://msdn.microsoft.com/aa6bc5cd-ec6a-4b8d-ab85-0131e0031a4b">GlobalPartitionID</a>


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

<a href="https://msdn.microsoft.com/6c5371e2-c196-4a98-9738-bbf3c456c36e">Is64BitCatalogServer</a>


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

<a href="https://msdn.microsoft.com/d290ec47-a2df-4de3-8719-cceeb893557d">IsApplicationInstanceDumpSupported</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the software required for application instance dumps is installed.

</td>
</tr>
</table> 

