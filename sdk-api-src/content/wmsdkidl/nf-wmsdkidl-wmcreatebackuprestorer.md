---
UID: NF:wmsdkidl.WMCreateBackupRestorer
title: WMCreateBackupRestorer function (wmsdkidl.h)
description: The WMCreateBackupRestorer function creates a backup restorer object.
helpviewer_keywords: ["WMCreateBackupRestorer","WMCreateBackupRestorer function [windows Media Format]","wmformat.wmcreatebackuprestorer","wmsdkidl/WMCreateBackupRestorer"]
old-location: wmformat\wmcreatebackuprestorer.htm
tech.root: wmformat
ms.assetid: 529a5066-df03-4747-bca5-10e3f223d4d2
ms.date: 12/05/2018
ms.keywords: WMCreateBackupRestorer, WMCreateBackupRestorer function [windows Media Format], wmformat.wmcreatebackuprestorer, wmsdkidl/WMCreateBackupRestorer
f1_keywords:
- wmsdkidl/WMCreateBackupRestorer
dev_langs:
- c++
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Wmvcore.dll
api_name:
- WMCreateBackupRestorer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WMCreateBackupRestorer function


## -description



The <b>WMCreateBackupRestorer</b> function creates a backup restorer object.




## -parameters




### -param pCallback [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface containing the <b>OnStatus</b> callback method to be used by the new backup restorer object.


### -param ppBackup [out]

Pointer to a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup</a> interface of the newly created backup restorer object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -remarks



Use <b>IWMLicenseBackup::QueryInterface</b> to obtain a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps</a> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/backup-restorer-object">Backup Restorer Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/functions">Functions</a>
 

 

