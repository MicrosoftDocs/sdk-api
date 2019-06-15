---
UID: NN:gpmgmt.IGPMMigrationTable
title: IGPMMigrationTable (gpmgmt.h)
author: windows-sdk-content
description: The IGPMMigrationTable interface provides an interface to a migration table.
old-location: gpmc\igpmmigrationtable.htm
tech.root: gpmc
ms.assetid: c80c76b0-8589-4ecb-b9bf-6b8377fa98dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMMigrationTable, IGPMMigrationTable, IGPMMigrationTable interface [GPMC], IGPMMigrationTable interface [GPMC],described, gpmc.igpmmigrationtable, gpmgmt/IGPMMigrationTable
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
ms.custom: 19H1
---

# IGPMMigrationTable interface


## -description


The <b>IGPMMigrationTable</b> interface provides an interface to a migration table.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMMigrationTable</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMMigrationTable</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-add">Add</a>
</td>
<td align="left" width="63%">
Adds the entries from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a> or the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a> interfaces.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-addentry">AddEntry</a>
</td>
<td align="left" width="63%">
Creates an entry if one does not already exist. The method  replaces an existing entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-deleteentry">DeleteEntry</a>
</td>
<td align="left" width="63%">
Deletes the entry from the migration table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-getentries">GetEntries</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmmapentrycollection">IGPMMapEntryCollection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-getentry">GetEntry</a>
</td>
<td align="left" width="63%">
Gets the entry in the migration table given the source field.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-save">Save</a>
</td>
<td align="left" width="63%">
Saves the migration table in the specified location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-updatedestination">UpdateDestination</a>
</td>
<td align="left" width="63%">
Updates the destination field of an entry in the migration table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmmigrationtable-validate">Validate</a>
</td>
<td align="left" width="63%">
Validates the migration table.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

