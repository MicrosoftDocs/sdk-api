---
UID: NN:comadmin.ICOMAdminCatalog
title: ICOMAdminCatalog
author: windows-sdk-content
description: Initiates a session to do programmatic COM+ administration, access collections in the catalog, install COM+ applications and components, start and stop services, and connect to remote servers.
old-location: cos\icomadmincatalog.htm
old-project: cossdk
ms.assetid: 2c3c49df-9ca5-40ea-b45c-f4eca1004602
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICOMAdminCatalog, ICOMAdminCatalog interface [COM+], ICOMAdminCatalog interface [COM+],described, comadmin/ICOMAdminCatalog, cos.icomadmincatalog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comadmin.h
req.include-header: 
req.redist: 
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

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICOMAdminCatalog</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICOMAdminCatalog</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms687013(v=VS.85).aspx">BackupREGDB</a>
</td>
<td align="left" width="63%">
Backs up the COM+ class registration database to a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678944(v=VS.85).aspx">Connect</a>
</td>
<td align="left" width="63%">
Connects to the COM+ catalog on a specified remote computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680628(v=VS.85).aspx">ExportApplication</a>
</td>
<td align="left" width="63%">
Exports a COM+ application or application proxy to a file, ready for installation on different computers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682306(v=VS.85).aspx">GetCollection</a>
</td>
<td align="left" width="63%">
Retrieves a top-level collection on the COM+ catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682302(v=VS.85).aspx">GetCollectionByQuery</a>
</td>
<td align="left" width="63%">
Retrieves a collection on the COM+ catalog given the key property values for all of its parent items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685051(v=VS.85).aspx">GetEventClassesForIID</a>
</td>
<td align="left" width="63%">
Retrieves a list of the event classes registered on the computer that implement a specified interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms687049(v=VS.85).aspx">GetMultipleComponentsInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the components found in the specified files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678934(v=VS.85).aspx">ImportComponent</a>
</td>
<td align="left" width="63%">
Imports a component already registered as an in-process server into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681806(v=VS.85).aspx">InstallApplication</a>
</td>
<td align="left" width="63%">
Installs a COM+ application or application proxy from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681794(v=VS.85).aspx">InstallComponent</a>
</td>
<td align="left" width="63%">
Installs all components (COM classes) from a DLL file into a COM+ application and registers the components in the COM+ class registration database.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684187(v=VS.85).aspx">InstallEventClass</a>
</td>
<td align="left" width="63%">
Installs event classes from a file into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682771(v=VS.85).aspx">InstallMultipleComponents</a>
</td>
<td align="left" width="63%">
Installs components from multiple files into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms678960(v=VS.85).aspx">InstallMultipleEventClasses</a>
</td>
<td align="left" width="63%">
Installs event classes from multiple files into a COM+ application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681751(v=VS.85).aspx">QueryApplicationFile</a>
</td>
<td align="left" width="63%">
Retrieves information about a COM+ application from an application file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681284(v=VS.85).aspx">RefreshComponents</a>
</td>
<td align="left" width="63%">
Updates component registration information from the registry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679866(v=VS.85).aspx">RefreshRouter</a>
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
<a href="https://msdn.microsoft.com/en-us/library/ms683256(v=VS.85).aspx">RestoreREGDB</a>
</td>
<td align="left" width="63%">
Restores the COM+ class registration database (RegDB) from the specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686864(v=VS.85).aspx">ServiceCheck</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the specified COM+ service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms682812(v=VS.85).aspx">ShutdownApplication</a>
</td>
<td align="left" width="63%">
Initiates shutdown of a COM+ server application process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683630(v=VS.85).aspx">StartApplication</a>
</td>
<td align="left" width="63%">
Starts the specified COM+ server application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679532(v=VS.85).aspx">StartRouter</a>
</td>
<td align="left" width="63%">
Starts the component load balancing service if the service is currently installed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679262(v=VS.85).aspx">StopRouter</a>
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

<a href="https://msdn.microsoft.com/en-us/library/ms686464(v=VS.85).aspx">MajorVersion</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms679471(v=VS.85).aspx">MinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the minor version number of the COMAdmin library.

</td>
</tr>
</table> 

