---
UID: NN:gpmgmt.IGPMBackup
title: IGPMBackup
author: windows-sdk-content
description: The IGPMBackup interface supports methods that allow you to delete GPMBackup objects and to retrieve various properties of GPMBackup objects.
old-location: gpmc\igpmbackup.htm
old-project: gpmc
ms.assetid: a593740a-9541-465a-9a2d-64ddf29793bf
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: GPMBackup, IGPMBackup, IGPMBackup interface [GPMC], IGPMBackup interface [GPMC],described, _win32_igpmbackup, gpmc.igpmbackup, gpmgmt/IGPMBackup
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMBackup
 - GPMBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMBackup interface


## -description


The 
<b>IGPMBackup</b> interface supports methods that allow you to delete 
<b>GPMBackup</b> objects and to retrieve various properties of <b>GPMBackup</b> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackup</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IGPMBackup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMBackup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/096f10ca-1528-4ce7-a135-6fc0007e3374">Delete</a>
</td>
<td align="left" width="63%">
Removes the GPO backup from the backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d5daa512-547f-4b2d-85b3-0f6e9244acb2">GenerateReport</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cba43c59-54d8-4d0b-b603-638f493cdf71">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO and then saves it to a file in a specified path.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackup</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">BackupDir</a>


</td>
<td align="left" width="63%">
The directory in which the <b>GPMBackup</b> object exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">Comment</a>


</td>
<td align="left" width="63%">
Comment associated with the <b>GPMBackup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">GPODisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the backed-up GPO. More than one GPO can have the same friendly name. The GPOs are identified in the directory service by the ID (GUID), not by the friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">GPODomain</a>


</td>
<td align="left" width="63%">
Name of the domain in which the GPO existed when it was backed up. This is a full Domain Name System (DNS) name, such as example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">GPOID</a>


</td>
<td align="left" width="63%">
ID of the backed-up GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">ID</a>


</td>
<td align="left" width="63%">
GUID that uniquely identifies the <b>GPMBackup</b> object within its backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">Timestamp</a>


</td>
<td align="left" width="63%">
Date and time when the <b>GPMBackup</b> object was created, in local time.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/2780760e-7114-46b0-a264-00ed58a556cb">IGPM</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMBackupCollection</a>



<a href="https://msdn.microsoft.com/2d44cf6d-a3fa-43db-b28e-3d48f6d13625">IGPMBackupDir</a>
 

 

