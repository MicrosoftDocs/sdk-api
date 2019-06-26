---
UID: NN:gpmgmt.IGPMBackupDir
title: IGPMBackupDir (gpmgmt.h)
author: windows-sdk-content
description: The IGPMBackupDir interface supports methods that allow you to query GPMBackup and GPMBackupCollection objects when you use the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmbackupdir.htm
tech.root: gpmc
ms.assetid: 2d44cf6d-a3fa-43db-b28e-3d48f6d13625
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMBackupDir, IGPMBackupDir, IGPMBackupDir interface [GPMC], IGPMBackupDir interface [GPMC],described, _win32_igpmbackupdir, gpmc.igpmbackupdir, gpmgmt/IGPMBackupDir
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMBackupDir"
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
ms.custom: 19H1
---

# IGPMBackupDir interface


## -description


The 
<b>IGPMBackupDir</b> interface supports methods that allow you to query 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> and 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a> objects when you use the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDir</b> object, call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getbackupdir">IGPM::GetBackupDir</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDir</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackupDir</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdir-getbackup">GetBackup</a>
</td>
<td align="left" width="63%">
Retrieves the <b>GPMBackup</b> object that has the specified backup ID (GUID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdir-searchbackups">SearchBackups</a>
</td>
<td align="left" width="63%">
Executes a search for <b>GPMBackup</b> objects according to search criteria, and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMBackupCollection</a> object.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackupdir-property-methods">BackupDirectory</a>


</td>
<td align="left" width="63%">
Full path of the file system directory for Group Policy object (GPO) backups.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>
 

 

