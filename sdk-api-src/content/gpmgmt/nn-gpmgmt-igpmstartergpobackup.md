---
UID: NN:gpmgmt.IGPMStarterGPOBackup
title: IGPMStarterGPOBackup (gpmgmt.h)
description: The IGPMStarterGPOBackup interface supports methods that allow you to delete GPMStarterGPOBackup objects and to retrieve various properties of GPMStarterGPOBackup objects.
helpviewer_keywords: ["GPMStarterGPOBackup","IGPMStarterGPOBackup","IGPMStarterGPOBackup interface [GPMC]","IGPMStarterGPOBackup interface [GPMC]","described","gpmc.igpmstartergpobackup","gpmgmt/IGPMStarterGPOBackup"]
old-location: gpmc\igpmstartergpobackup.htm
tech.root: gpmc
ms.assetid: b062da03-6d9c-42b3-a4aa-5a7a6a38e4c9
ms.date: 12/05/2018
ms.keywords: GPMStarterGPOBackup, IGPMStarterGPOBackup, IGPMStarterGPOBackup interface [GPMC], IGPMStarterGPOBackup interface [GPMC],described, gpmc.igpmstartergpobackup, gpmgmt/IGPMStarterGPOBackup
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMStarterGPOBackup
 - gpmgmt/IGPMStarterGPOBackup
dev_langs:
 - c++
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
---

# IGPMStarterGPOBackup interface


## -description

The 
<b>IGPMStarterGPOBackup</b> interface supports methods that allow you to delete 
<b>GPMStarterGPOBackup</b> objects and to retrieve various properties of <b>GPMStarterGPOBackup</b> objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMStarterGPOBackup</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMStarterGPOBackup</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpobackup-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the GPO backup from the backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpobackup-generatereport">GenerateReport</a>
</td>
<td align="left" width="63%">
Gets the report for the backup GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmstartergpobackup-generatereporttofile">GenerateReportToFile</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">BackupDir</a>


</td>
<td align="left" width="63%">
The directory in which the <b>GPMStarterGPOBackup</b> object exists.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">Comment</a>


</td>
<td align="left" width="63%">
Comment associated with the <b>GPMStarterGPOBackup</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpobackup-property-methods">DisplayName</a>


</td>
<td align="left" width="63%">
Friendly display name of the backed-up GPO. Note that it is possible to have more than one GPO with the same friendly name; GPOs are identified in the Directory Service by ID (GUID), not by friendly name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmstartergpobackup-property-methods">Domain</a>


</td>
<td align="left" width="63%">
Name of the domain in which the GPO existed when it was backed up. This is a full DNS name, such as, example.microsoft.com.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">ID</a>


</td>
<td align="left" width="63%">
GUID that uniquely identifies the <b>GPMStarterGPOBackup</b> object within its backup directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">StarterGPOID</a>


</td>
<td align="left" width="63%">
ID of the backed-up GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">Timestamp</a>


</td>
<td align="left" width="63%">
Date and time when the <b>GPMStarterGPOBackup</b> object was created, in local time.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackup-property-methods">Type</a>


</td>
<td align="left" width="63%">
Retrieves the value of the <b>Type</b> property representing a system or custom Starter Group Policy object.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm2">IGPM2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupdirex">IGPMBackupDirEx</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMStarterGPOBackupCollection</a>

