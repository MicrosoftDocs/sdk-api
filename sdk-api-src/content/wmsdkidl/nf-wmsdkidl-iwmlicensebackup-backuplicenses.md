---
UID: NF:wmsdkidl.IWMLicenseBackup.BackupLicenses
title: IWMLicenseBackup::BackupLicenses (wmsdkidl.h)
description: The BackupLicenses method saves copies of the licenses.
helpviewer_keywords: ["BackupLicenses","BackupLicenses method [windows Media Format]","BackupLicenses method [windows Media Format]","IWMLicenseBackup interface","IWMLicenseBackup interface [windows Media Format]","BackupLicenses method","IWMLicenseBackup.BackupLicenses","IWMLicenseBackup::BackupLicenses","IWMLicenseBackupBackupLicenses","wmformat.iwmlicensebackup_backuplicenses","wmsdkidl/IWMLicenseBackup::BackupLicenses"]
old-location: wmformat\iwmlicensebackup_backuplicenses.htm
tech.root: wmformat
ms.assetid: 714971d7-8ccb-41fa-92b2-802a503ae228
ms.date: 12/05/2018
ms.keywords: BackupLicenses, BackupLicenses method [windows Media Format], BackupLicenses method [windows Media Format],IWMLicenseBackup interface, IWMLicenseBackup interface [windows Media Format],BackupLicenses method, IWMLicenseBackup.BackupLicenses, IWMLicenseBackup::BackupLicenses, IWMLicenseBackupBackupLicenses, wmformat.iwmlicensebackup_backuplicenses, wmsdkidl/IWMLicenseBackup::BackupLicenses
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMLicenseBackup::BackupLicenses
 - wmsdkidl/IWMLicenseBackup::BackupLicenses
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMLicenseBackup.BackupLicenses
---

# IWMLicenseBackup::BackupLicenses


## -description

<p class="CCE_Message">[<b>BackupLicenses</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>BackupLicenses</b> method saves copies of the licenses.

## -parameters

### -param dwFlags [in]

<b>DWORD</b> containing the flags.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WM_BACKUP_OVERWRITE</td>
<td>Indicates that any existing backup file should be overwritten. If this is not set, and a backup file exists, the NS_E_DRM_BACKUP_EXISTS error code is returned.</td>
</tr>
</table>

### -param pCallback [in]

Pointer to an object that implements the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallback</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory available to perform the task.

</td>
</tr>
</table>

## -remarks

For more information on how to specify the location of the backup file (there are predefined properties for the backup path and restore path for this purpose), see <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>.

This method operates asynchronously, and an <b>IWMStatusCallback</b> object can be used to track progress.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup Interface</a>