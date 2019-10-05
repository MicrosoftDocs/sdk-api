---
UID: NN:gpmgmt.IGPMBackupDirEx
title: IGPMBackupDirEx (gpmgmt.h)
author: windows-sdk-content
description: The IGPMBackupDirEx interface supports methods that allow you to query GPMBackup, GPMBackupCollection, GPMStarterGPOBackup, and GPMStarterGPOBackupCollection objects when you are using the Group Policy Management Console (GPMC) interfaces.
old-location: gpmc\igpmbackupdirex.htm
tech.root: gpmc
ms.assetid: 3008e70c-cc34-45b0-bdfc-17f2e9cd5de0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPMBackupDirEx, IGPMBackupDirEx, IGPMBackupDirEx interface [GPMC], IGPMBackupDirEx interface [GPMC],described, gpmc.igpmbackupdirex, gpmgmt/IGPMBackupDirEx
ms.topic: interface
f1_keywords: 
 - "gpmgmt/IGPMBackupDirEx"
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
 - IGPMBackupDirEx
 - GPMBackupDirEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPMBackupDirEx interface


## -description


The 
<b>IGPMBackupDirEx</b> interface supports methods that allow you to query 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a>,  
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">GPMBackupCollection</a>, <b>GPMStarterGPOBackup</b>,  
and <b>GPMStarterGPOBackupCollection</b>    objects when you are using the Group Policy Management Console (GPMC) interfaces.

To create a <b>GPMBackupDirEx</b> object, call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpm-getbackupdir">IGPM2::GetBackupDirEx</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPMBackupDirEx</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMBackupDirEx</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdirex-getbackup">GetBackup</a>
</td>
<td align="left" width="63%">
Retrieves the <b>GPMBackup</b> or a Starter Group Policy object (GPO) backup <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMStarterGPOBackup</a> object with the specified backup ID (GUID).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nf-gpmgmt-igpmbackupdirex-searchbackups">SearchBackups</a>
</td>
<td align="left" width="63%">
Executes a search for <b>GPMBackup</b> or <b>GPMStarterGPOBackup</b> objects according to the specified search criteria, and returns a 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpocollection">GPMBackupCollection</a> or <b>GPMStarterGPOBackupCollection</b> object.

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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackupdir-property-methods">BackupDirectory</a>


</td>
<td align="left" width="63%">
Pointer to the  path of the file system directory for Group Policy object (GPO) backups.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/gpmc/igpmbackupdir-property-methods">BackupType</a>


</td>
<td align="left" width="63%">
Value that specifies whether the  specified backup is a Group Policy object (GPO) backup  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">GPMBackup</a> or a Starter Group Policy object (GPO) backup <b>GPMStarterGPOBackup</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackup">IGPMBackup</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmbackupcollection">IGPMBackupCollection</a>



<b>IGPMStarterGPOBackup</b>



<b>IGPMStarterGPOBackupCollection</b>
 

 

