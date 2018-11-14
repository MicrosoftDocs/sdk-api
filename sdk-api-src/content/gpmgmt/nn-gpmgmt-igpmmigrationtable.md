---
UID: NN:gpmgmt.IGPMMigrationTable
title: IGPMMigrationTable
author: windows-sdk-content
description: The IGPMMigrationTable interface provides an interface to a migration table.
old-location: gpmc\igpmmigrationtable.htm
tech.root: GPMC
ms.assetid: c80c76b0-8589-4ecb-b9bf-6b8377fa98dd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPMMigrationTable, IGPMMigrationTable, IGPMMigrationTable interface [GPMC], IGPMMigrationTable interface [GPMC],described, gpmc.igpmmigrationtable, gpmgmt/IGPMMigrationTable
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
 - IGPMMigrationTable
 - GPMMigrationTable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPMMigrationTable interface


## -description


The <b>IGPMMigrationTable</b> interface provides an interface to a migration table.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMMigrationTable</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IGPMMigrationTable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPMMigrationTable</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7be82b5-acb5-4e08-9771-d2698df3d0df">Add</a>
</td>
<td align="left" width="63%">
Adds the entries from the <a href="https://msdn.microsoft.com/2857c8b7-019d-4ec2-9a00-574fc8541cae">IGPMGPO</a> or the <a href="https://msdn.microsoft.com/a593740a-9541-465a-9a2d-64ddf29793bf">IGPMBackup</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e6f6b81-b01c-4d46-9b7b-3265580f112a">AddEntry</a>
</td>
<td align="left" width="63%">
Creates an entry if one does not already exist. The method  replaces an existing entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/712a6419-2f64-4657-993a-e7f6bfc1259e">DeleteEntry</a>
</td>
<td align="left" width="63%">
Deletes the entry from the migration table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5de22bba-10f9-49f7-83f3-053f5e58b66e">GetEntries</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/a017ff4b-ab3c-4da9-b6c9-b4ccd24230eb">IGPMMapEntryCollection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d6985ab-dbea-446c-9666-5fa19b97b40c">GetEntry</a>
</td>
<td align="left" width="63%">
Gets the entry in the migration table given the source field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce33306a-c72f-4231-a19c-eb733d87b361">Save</a>
</td>
<td align="left" width="63%">
Saves the migration table in the specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c47ad9d7-cf04-4ab4-9c44-78a5e54fc04e">UpdateDestination</a>
</td>
<td align="left" width="63%">
Updates the destination field of an entry in the migration table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b442155-3dd7-4a74-ad33-db79114459ac">Validate</a>
</td>
<td align="left" width="63%">
Validates the migration table.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

