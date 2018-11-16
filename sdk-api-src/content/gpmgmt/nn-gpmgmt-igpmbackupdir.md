---
UID: NN:gpmgmt.IGPMBackupDir
title: IGPMBackupDir
author: windows-sdk-content
description: The IGPMBackupDir interface supports methods that allow you to query GPMBackup and GPMBackupCollection objects when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmbackupdir.htm
tech.root: GPMC
ms.assetid: 2d44cf6d-a3fa-43db-b28e-3d48f6d13625
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GPMBackupDir, IGPMBackupDir, IGPMBackupDir interface [GPMC], IGPMBackupDir interface [GPMC],described, _win32_igpmbackupdir, gpmc.igpmbackupdir, gpmgmt/IGPMBackupDir
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackupDir
 - GPMBackupDir
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMBackupDir interface


## -description


The 
<b>IGPMBackupDir</b> interface supports methods that allow you to query 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> and 
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a> objects when you use the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDir</b> object, call the 
<a href="https://msdn.microsoft.com/4ffc8827-8427-4ee5-ad89-21f821d16d97">IGPM::GetBackupDir</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDir</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMBackupDir</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMBackupDir</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45f286dc-fa60-4cfd-bdf0-bfeaf2a5a396">GetBackup</a>
</td>
<td align="left" width="63%">
Retrieves the <b>GPMBackup</b> object that has the specified backup ID (GUID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71e1991f-c24f-43fe-8f3e-83f5b02cec6b">SearchBackups</a>
</td>
<td align="left" width="63%">
Executes a search for <b>GPMBackup</b> objects according to search criteria, and returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMBackupCollection</a> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDir</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/303bdd12-9c45-4722-a737-da318e84a735">BackupDirectory</a>


</td>
<td align="left" width="63%">
Full path of the file system directory for Group Policy object (GPO) backups.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>
 

 

