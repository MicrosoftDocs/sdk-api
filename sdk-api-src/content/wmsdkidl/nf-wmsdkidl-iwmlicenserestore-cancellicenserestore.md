---
UID: NF:wmsdkidl.IWMLicenseRestore.CancelLicenseRestore
title: IWMLicenseRestore::CancelLicenseRestore (wmsdkidl.h)
description: The CancelLicenseRestore method cancels a current restore operation.
helpviewer_keywords: ["CancelLicenseRestore","CancelLicenseRestore method [windows Media Format]","CancelLicenseRestore method [windows Media Format]","IWMLicenseRestore interface","IWMLicenseRestore interface [windows Media Format]","CancelLicenseRestore method","IWMLicenseRestore.CancelLicenseRestore","IWMLicenseRestore::CancelLicenseRestore","IWMLicenseRestoreCancelLicenseRestore","wmformat.iwmlicenserestore_cancellicenserestore","wmsdkidl/IWMLicenseRestore::CancelLicenseRestore"]
old-location: wmformat\iwmlicenserestore_cancellicenserestore.htm
tech.root: wmformat
ms.assetid: b8a39804-5ee6-43ab-8e89-d1008217622d
ms.date: 4/26/2023
ms.keywords: CancelLicenseRestore, CancelLicenseRestore method [windows Media Format], CancelLicenseRestore method [windows Media Format],IWMLicenseRestore interface, IWMLicenseRestore interface [windows Media Format],CancelLicenseRestore method, IWMLicenseRestore.CancelLicenseRestore, IWMLicenseRestore::CancelLicenseRestore, IWMLicenseRestoreCancelLicenseRestore, wmformat.iwmlicenserestore_cancellicenserestore, wmsdkidl/IWMLicenseRestore::CancelLicenseRestore
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
 - IWMLicenseRestore::CancelLicenseRestore
 - wmsdkidl/IWMLicenseRestore::CancelLicenseRestore
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
 - IWMLicenseRestore.CancelLicenseRestore
---

# IWMLicenseRestore::CancelLicenseRestore


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>CancelLicenseRestore</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>CancelLicenseRestore</b> method cancels a current restore operation.



## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method operates asynchronously, and a call to this method cancels a restore operation that is in progress.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore">IWMLicenseRestore Interface</a>
