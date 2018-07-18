---
UID: NN:comadmin.ICOMAdminCatalog
title: ICOMAdminCatalog
author: windows-sdk-content
description: Initiates a session to do programmatic COM+ administration, access collections in the catalog, install COM+ applications and components, start and stop services, and connect to remote servers.
old-location: cos\icomadmincatalog.htm
old-project: cossdk
ms.assetid: 2c3c49df-9ca5-40ea-b45c-f4eca1004602
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ICOMAdminCatalog, ICOMAdminCatalog interface [COM+], ICOMAdminCatalog interface [COM+],described, comadmin/ICOMAdminCatalog, cos.icomadmincatalog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComAdmin.h
api_name:
 - ICOMAdminCatalog
 - ICOMAdminCatalog.Reserved1
 - ICOMAdminCatalog.Reserved2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICOMAdminCatalog interface


## -description


Initiates a session to do programmatic COM+ administration, access collections in the catalog, install COM+ applications and components, start and stop services, and connect to remote servers. <b>ICOMAdminCatalog</b> provides access to the COM+ catalog data store.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICOMAdminCatalog</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICOMAdminCatalog</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd350abd-3b59-4a5d-b2e4-1ddeec2b1953">BackupREGDB</a>
</td>
<td align="left" width="63%">
Backs up the COM+ class registration database to a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fc65ec0-79a7-4544-934d-543f2946c70a">Connect</a>
</td>
<td align="left" width="63%">
Connects to the COM+ catalog on a specified remote computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/431c0299-56c2-4ec3-8ecc-ee1cbec3eff6">ExportApplication</a>
</td>
<td align="left" width="63%">
Exports a COM+ application or application proxy to a file, ready for installation on different computers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f01a7a7-d8f3-470f-8eb3-aa698b353af1">GetCollection</a>
</td>
<td align="left" width="63%">
Retrieves a top-level collection on the COM+ catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ec65e7c-fb67-4435-90cd-d17b8fbcbc84">GetCollectionByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f1a77ef-3dfd-4402-a05a-9cb4fd50dbd8">GetEventClassesForIID</a>
</td>
<td align="left" width="63%">
Retrieves a list of the event classes registered on the computer that implement a specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd8c5975-c67a-4f1b-9d48-25053ba5c0e9">GetMultipleComponentsInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the components found in the specified files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e29025d-60bc-4f95-a6f9-aa178769855c">ImportComponent</a>
</td>
<td align="left" width="63%">
Imports a component already registered as an in-process server into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/668f73e1-7238-42f5-b68c-a0b0c2595d18">InstallApplication</a>
</td>
<td align="left" width="63%">
Installs a COM+ application or application proxy from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63af9aa4-a1f0-4277-bd36-8b4c64227b3f">InstallComponent</a>
</td>
<td align="left" width="63%">
Installs all components (COM classes) from a DLL file into a COM+ application and registers the components in the COM+ class registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e9f7c79-076e-46dc-bce0-389c5309e6fa">InstallEventClass</a>
</td>
<td align="left" width="63%">
Installs event classes from a file into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7206c93b-43ca-402f-9a55-930f872d4201">InstallMultipleComponents</a>
</td>
<td align="left" width="63%">
Installs components from multiple files into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12860254-4658-4e0d-ad00-7e25875037bf">InstallMultipleEventClasses</a>
</td>
<td align="left" width="63%">
Installs event classes from multiple files into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f90da9d-06eb-4ec0-8ea1-d040c8e084b7">QueryApplicationFile</a>
</td>
<td align="left" width="63%">
Retrieves information about a COM+ application from an application file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50528312-60e1-4648-b0e5-709a6b49737e">RefreshComponents</a>
</td>
<td align="left" width="63%">
Updates component registration information from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37947fb5-a1d0-445b-97f0-ceb711ed81b4">RefreshRouter</a>
</td>
<td align="left" width="63%">
Obsolete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Reserved1</b></td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Reserved2</b></td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7cb2201c-601c-4add-8608-3f98ef92c26d">RestoreREGDB</a>
</td>
<td align="left" width="63%">
Restores the COM+ class registration database (RegDB) from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7d41691-30ab-450c-b93b-b7b02f408eb1">ServiceCheck</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the specified COM+ service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79f3af18-0924-4e09-85aa-54a6886b65b3">ShutdownApplication</a>
</td>
<td align="left" width="63%">
Initiates shutdown of a COM+ server application process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89423f39-7cbd-42dd-8d4a-6f312884e0bf">StartApplication</a>
</td>
<td align="left" width="63%">
Starts the specified COM+ server application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d2c0ee0-2758-4d69-878a-78ce216a9201">StartRouter</a>
</td>
<td align="left" width="63%">
Starts the component load balancing service if the service is currently installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23b0e4af-bdab-4f58-b3ab-82aab5516b48">StopRouter</a>
</td>
<td align="left" width="63%">
Stops the component load balancing service if the service is currently installed.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/caa82b0e-435d-4d98-bef0-cd823213c518">MajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the major version number of the COMAdmin library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/25053a37-f44a-4e30-97b2-081b840c4448">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minor version number of the COMAdmin library.

</td>
</tr>
</table> 

