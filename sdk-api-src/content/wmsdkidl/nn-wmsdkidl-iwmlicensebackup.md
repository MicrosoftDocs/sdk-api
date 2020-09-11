---
UID: NN:wmsdkidl.IWMLicenseBackup
title: IWMLicenseBackup (wmsdkidl.h)
description: The IWMLicenseBackup interface manages the backing up of licenses, typically so that they can be restored onto another computer.This interface is obtained by using the WMCreateBackupRestorer function.
helpviewer_keywords: ["IWMLicenseBackup","IWMLicenseBackup interface [windows Media Format]","IWMLicenseBackup interface [windows Media Format]","described","IWMLicenseBackupInterface","wmformat.iwmlicensebackup","wmsdkidl/IWMLicenseBackup"]
old-location: wmformat\iwmlicensebackup.htm
tech.root: wmformat
ms.assetid: 4ef43b7e-706b-48f6-80ba-7d0a59c3929a
ms.date: 12/05/2018
ms.keywords: IWMLicenseBackup, IWMLicenseBackup interface [windows Media Format], IWMLicenseBackup interface [windows Media Format],described, IWMLicenseBackupInterface, wmformat.iwmlicensebackup, wmsdkidl/IWMLicenseBackup
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMLicenseBackup
 - wmsdkidl/IWMLicenseBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMLicenseBackup
---

# IWMLicenseBackup interface


## -description

<p class="CCE_Message">[<b>IWMLicenseBackup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMLicenseBackup</b> interface manages the backing up of licenses, typically so that they can be restored onto another computer.

This interface is obtained by using the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer">WMCreateBackupRestorer</a> function.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMLicenseBackup</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLicenseBackup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMLicenseBackup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses">BackupLicenses</a>
</td>
<td align="left" width="63%">
Saves copies of the licenses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicensebackup-cancellicensebackup">CancelLicenseBackup</a>
</td>
<td align="left" width="63%">
Cancels a current backup operation.

</td>
</tr>
</table> 

The following interfaces can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps</a>
</td>
<td>IID_IWMBackupRestoreProps</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore</a>
</td>
<td>IID_IWMLicenseRestore</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/wmformat/backing-up-and-restoring-licenses">Backing Up and Restoring Licenses</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/backup-restorer-object">Backup Restorer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>

