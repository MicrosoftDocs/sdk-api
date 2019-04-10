---
UID: NN:gpmgmt.IGPMStarterGPOBackup
title: IGPMStarterGPOBackup (gpmgmt.h)
author: windows-sdk-content
description: The IGPMStarterGPOBackup interface supports methods that allow you to delete GPMStarterGPOBackup objects and to retrieve various properties of GPMStarterGPOBackup objects.
old-location: gpmc\igpmstartergpobackup.htm
tech.root: gpmc
ms.assetid: b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMStarterGPOBackup, IGPMStarterGPOBackup, IGPMStarterGPOBackup interface [GPMC], IGPMStarterGPOBackup interface [GPMC],described, gpmc.igpmstartergpobackup, gpmgmt/IGPMStarterGPOBackup
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
 - IGPMStarterGPOBackup
 - GPMStarterGPOBackup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMStarterGPOBackup interface


## -description


The 
<b>IGPMStarterGPOBackup</b> interface supports methods that allow you to delete 
<b>GPMStarterGPOBackup</b> objects and to retrieve various properties of <b>GPMStarterGPOBackup</b> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackup</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMStarterGPOBackup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IGPMStarterGPOBackup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32a1388a-b8b9-455b-af94-0a09e98f9108">Delete</a>
</td>
<td align="left" width="63%">
Removes the GPO backup from the backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce0dd44f-dfd9-4e7c-9854-9decbc25ec54">GenerateReport</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7d05436-acd7-4b80-93e4-ea80e3eb1fff">GenerateReportToFile</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO and saves it to a file at a specified path.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackup</b> interface has these properties.
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
The directory in which the <b>GPMStarterGPOBackup</b> object exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">Comment</a>


</td>
<td align="left" width="63%">
Comment associated with the <b>GPMStarterGPOBackup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d12b7893-00d2-42cb-8fa4-b200a2d4b340">DisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the backed-up GPO. Note that it is possible to have more than one GPO with the same friendly name; GPOs are identified in the Directory Service by ID (GUID), not by friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d12b7893-00d2-42cb-8fa4-b200a2d4b340">Domain</a>


</td>
<td align="left" width="63%">
Name of the domain in which the GPO existed when it was backed up. This is a full DNS name, such as, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">ID</a>


</td>
<td align="left" width="63%">
GUID that uniquely identifies the <b>GPMStarterGPOBackup</b> object within its backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">StarterGPOID</a>


</td>
<td align="left" width="63%">
ID of the backed-up GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">Timestamp</a>


</td>
<td align="left" width="63%">
Date and time when the <b>GPMStarterGPOBackup</b> object was created, in local time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5393a50a-ce4c-436d-9e86-2f9540652d6a">Type</a>


</td>
<td align="left" width="63%">
Retrieves the value of the <b>Type</b> property representing a system or custom Starter Group Policy object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/f9cd432a-3974-4fc4-9e32-1d8e2df1601c">IGPM2</a>



<a href="https://msdn.microsoft.com/3008e70c-cc34-45b0-bdfc-17f2e9cd5de0">IGPMBackupDirEx</a>



<a href="https://msdn.microsoft.com/cd9e6b58-6fbc-449a-9941-b33761797199">IGPMStarterGPOBackupCollection</a>
 

 

