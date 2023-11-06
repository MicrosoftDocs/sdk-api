---
UID: NN:wmsdkidl.IWMStatusCallback
title: IWMStatusCallback (wmsdkidl.h)
description: The IWMStatusCallback interface is implemented by the application to receive status information from various objects.
helpviewer_keywords: ["IWMStatusCallback","IWMStatusCallback interface [windows Media Format]","IWMStatusCallback interface [windows Media Format]","described","IWMStatusCallbackInterface","wmformat.iwmstatuscallback","wmsdkidl/IWMStatusCallback"]
old-location: wmformat\iwmstatuscallback.htm
tech.root: wmformat
ms.assetid: a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3
ms.date: 4/26/2023
ms.keywords: IWMStatusCallback, IWMStatusCallback interface [windows Media Format], IWMStatusCallback interface [windows Media Format],described, IWMStatusCallbackInterface, wmformat.iwmstatuscallback, wmsdkidl/IWMStatusCallback
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IWMStatusCallback
 - wmsdkidl/IWMStatusCallback
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
 - IWMStatusCallback
---

# IWMStatusCallback interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMStatusCallback</b> interface is implemented by the application to receive status information from various objects.

## -inheritance

The <b>IWMStatusCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStatusCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The following methods and functions associate an implementation of this interface with an object:

<ul>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing">IWMIndexer::StartIndexing</a>
</li>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses">IWMLicenseBackup::BackupLicenses</a>
</li>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses">IWMLicenseRestore::RestoreLicenses</a>
</li>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>
</li>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise">IWMRegisterCallback::Advise</a>
</li>
<li>
<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer">WMCreateBackupRestorer</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
