---
UID: NN:gpmgmt.IGPMBackup
title: IGPMBackup (gpmgmt.h)
description: The IGPMBackup interface supports methods that allow you to delete GPMBackup objects and to retrieve various properties of GPMBackup objects.
old-location: gpmc\igpmbackup.htm
tech.root: gpmc
ms.assetid: a593740a-9541-465a-9a2d-64ddf29793bf
ms.date: 12/05/2018
ms.keywords: GPMBackup, IGPMBackup, IGPMBackup interface [GPMC], IGPMBackup interface [GPMC],described, _win32_igpmbackup, gpmc.igpmbackup, gpmgmt/IGPMBackup
f1_keywords:
- gpmgmt/IGPMBackup
dev_langs:
- c++
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
- IGPMBackup
- GPMBackup
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMBackup interface


## -description


The 
<b>IGPMBackup</b> interface supports methods that allow you to delete 
<b>GPMBackup</b> objects and to retrieve various properties of <b>GPMBackup</b> objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackup</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the GPO backup from the backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereport">GenerateReport</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackup-generatereporttofile">GenerateReportToFile</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">BackupDir</a>


</td>
<td align="left" width="63%">
The directory in which the <b>GPMBackup</b> object exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">Comment</a>


</td>
<td align="left" width="63%">
Comment associated with the <b>GPMBackup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">GPODisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the backed-up GPO. More than one GPO can have the same friendly name. The GPOs are identified in the directory service by the ID (GUID), not by the friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">GPODomain</a>


</td>
<td align="left" width="63%">
Name of the domain in which the GPO existed when it was backed up. This is a full Domain Name System (DNS) name, such as example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">GPOID</a>


</td>
<td align="left" width="63%">
ID of the backed-up GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">ID</a>


</td>
<td align="left" width="63%">
GUID that uniquely identifies the <b>GPMBackup</b> object within its backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">Timestamp</a>


</td>
<td align="left" width="63%">
Date and time when the <b>GPMBackup</b> object was created, in local time.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdir">IGPMBackupDir</a>
 

 

