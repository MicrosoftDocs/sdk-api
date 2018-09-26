---
UID: NN:gpmgmt.IGPMBackupDirEx
title: IGPMBackupDirEx
author: windows-sdk-content
description: The IGPMBackupDirEx interface supports methods that allow you to query GPMBackup, GPMBackupCollection, GPMStarterGPOBackup, and GPMStarterGPOBackupCollection objects when you are using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmbackupdirex.htm
tech.root: GPMC
ms.assetid: 3008e70c-cc34-45b0-bdfc-17f2e9cd5de0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GPMBackupDirEx, IGPMBackupDirEx, IGPMBackupDirEx interface [GPMC], IGPMBackupDirEx interface [GPMC],described, gpmc.igpmbackupdirex, gpmgmt/IGPMBackupDirEx
ms.prod: windows
ms.technology: windows-sdk
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
 - IGPMBackupDirEx
 - GPMBackupDirEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMBackupDirEx interface


## -description


The 
<b>IGPMBackupDirEx</b> interface supports methods that allow you to query 
<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a>,  
<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">GPMBackupCollection</a>, <b>GPMStarterGPOBackup</b>,  
and <b>GPMStarterGPOBackupCollection</b>    objects when you are using the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDirEx</b> object, call the 
<a href="https://msdn.microsoft.com/4ffc8827-8427-4ee5-ad89-21f821d16d97">IGPM2::GetBackupDirEx</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDirEx</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMBackupDirEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMBackupDirEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1c6ead9-882d-4041-9586-f08a83f4c9b0">GetBackup</a>
</td>
<td align="left" width="63%">
Retrieves the <b>GPMBackup</b> or a Starter Group Policy object (GPO) backup <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMStarterGPOBackup</a> object with the specified backup ID (GUID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e45f012e-ce88-4baf-88a2-bd61e365b291">SearchBackups</a>
</td>
<td align="left" width="63%">
Executes a search for <b>GPMBackup</b> or <b>GPMStarterGPOBackup</b> objects according to the specified search criteria, and returns a 
<a href="https://msdn.microsoft.com/847aea86-48e9-428e-ae4d-e6a7e1e13428">GPMBackupCollection</a> or <b>GPMStarterGPOBackupCollection</b> object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDirEx</b> interface has these properties.
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
Pointer to the  path of the file system directory for Group Policy object (GPO) backups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/303bdd12-9c45-4722-a737-da318e84a735">BackupType</a>


</td>
<td align="left" width="63%">
Value that specifies whether the  specified backup is a Group Policy object (GPO) backup  <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">GPMBackup</a> or a Starter Group Policy object (GPO) backup <b>GPMStarterGPOBackup</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM2</a>



<a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
 

 

