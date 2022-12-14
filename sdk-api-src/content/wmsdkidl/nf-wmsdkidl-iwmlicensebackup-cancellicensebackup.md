---
UID: NF:wmsdkidl.IWMLicenseBackup.CancelLicenseBackup
title: IWMLicenseBackup::CancelLicenseBackup (wmsdkidl.h)
description: The CancelLicenseBackup method cancels a current backup operation.
helpviewer_keywords: ["CancelLicenseBackup","CancelLicenseBackup method [windows Media Format]","CancelLicenseBackup method [windows Media Format]","IWMLicenseBackup interface","IWMLicenseBackup interface [windows Media Format]","CancelLicenseBackup method","IWMLicenseBackup.CancelLicenseBackup","IWMLicenseBackup::CancelLicenseBackup","IWMLicenseBackupCancelLicenseBackup","wmformat.iwmlicensebackup_cancellicensebackup","wmsdkidl/IWMLicenseBackup::CancelLicenseBackup"]
old-location: wmformat\iwmlicensebackup_cancellicensebackup.htm
tech.root: wmformat
ms.assetid: aa226875-d59f-4fac-b38b-f94727fa2f4a
ms.date: 12/05/2018
ms.keywords: CancelLicenseBackup, CancelLicenseBackup method [windows Media Format], CancelLicenseBackup method [windows Media Format],IWMLicenseBackup interface, IWMLicenseBackup interface [windows Media Format],CancelLicenseBackup method, IWMLicenseBackup.CancelLicenseBackup, IWMLicenseBackup::CancelLicenseBackup, IWMLicenseBackupCancelLicenseBackup, wmformat.iwmlicensebackup_cancellicensebackup, wmsdkidl/IWMLicenseBackup::CancelLicenseBackup
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
 - IWMLicenseBackup::CancelLicenseBackup
 - wmsdkidl/IWMLicenseBackup::CancelLicenseBackup
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
 - IWMLicenseBackup.CancelLicenseBackup
---

# IWMLicenseBackup::CancelLicenseBackup


## -description

<p class="CCE_Message">[<b>CancelLicenseBackup</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>CancelLicenseBackup</b> method cancels a current backup operation.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

A backup operation is asynchronous, and a call to this method cancels a backup that is in progress.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup">IWMLicenseBackup Interface</a>
