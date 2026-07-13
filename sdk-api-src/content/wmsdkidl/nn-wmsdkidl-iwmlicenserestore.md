---
UID: NN:wmsdkidl.IWMLicenseRestore
title: IWMLicenseRestore (wmsdkidl.h)
description: The IWMLicenseRestore interface manages the restoring of licenses.This interface is obtained from another interface on the backup restorer object.
helpviewer_keywords: ["IWMLicenseRestore","IWMLicenseRestore interface [windows Media Format]","IWMLicenseRestore interface [windows Media Format]","described","IWMLicenseRestoreInterface","wmformat.iwmlicenserestore","wmsdkidl/IWMLicenseRestore"]
old-location: wmformat\iwmlicenserestore.htm
tech.root: wmformat
ms.assetid: 29444445-7104-4900-a00d-dabd2766d1d7
ms.date: 4/26/2023
ms.keywords: IWMLicenseRestore, IWMLicenseRestore interface [windows Media Format], IWMLicenseRestore interface [windows Media Format],described, IWMLicenseRestoreInterface, wmformat.iwmlicenserestore, wmsdkidl/IWMLicenseRestore
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
 - IWMLicenseRestore
 - wmsdkidl/IWMLicenseRestore
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
 - IWMLicenseRestore
---

# IWMLicenseRestore interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMLicenseRestore</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMLicenseRestore</b> interface manages the restoring of licenses.

This interface is obtained from another interface on the backup restorer object.

## -inheritance

The <b>IWMLicenseRestore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMLicenseRestore</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/backing-up-and-restoring-licenses">Backing Up and Restoring Licenses</a>



<a href="/windows/desktop/wmformat/backup-restorer-object">Backup Restorer Object</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops">IWMBackupRestoreProps Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
