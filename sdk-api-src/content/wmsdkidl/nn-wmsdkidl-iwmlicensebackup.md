---
UID: NN:wmsdkidl.IWMLicenseBackup
title: IWMLicenseBackup (wmsdkidl.h)
description: The IWMLicenseBackup interface manages the backing up of licenses, typically so that they can be restored onto another computer.This interface is obtained by using the WMCreateBackupRestorer function.
helpviewer_keywords: ["IWMLicenseBackup","IWMLicenseBackup interface [windows Media Format]","IWMLicenseBackup interface [windows Media Format]","described","IWMLicenseBackupInterface","wmformat.iwmlicensebackup","wmsdkidl/IWMLicenseBackup"]
old-location: wmformat\iwmlicensebackup.htm
tech.root: wmformat
ms.assetid: 4ef43b7e-706b-48f6-80ba-7d0a59c3929a
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMLicenseBackup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMLicenseBackup</b> interface manages the backing up of licenses, typically so that they can be restored onto another computer.

This interface is obtained by using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer">WMCreateBackupRestorer</a> function.

## -inheritance

The <b>IWMLicenseBackup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLicenseBackup</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/backing-up-and-restoring-licenses">Backing Up and Restoring Licenses</a>



<a href="/windows/desktop/wmformat/backup-restorer-object">Backup Restorer Object</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
