---
UID: NN:wmsdkidl.IWMStatusCallback
title: IWMStatusCallback (wmsdkidl.h)
description: The IWMStatusCallback interface is implemented by the application to receive status information from various objects.
helpviewer_keywords: ["IWMStatusCallback","IWMStatusCallback interface [windows Media Format]","IWMStatusCallback interface [windows Media Format]","described","IWMStatusCallbackInterface","wmformat.iwmstatuscallback","wmsdkidl/IWMStatusCallback"]
old-location: wmformat\iwmstatuscallback.htm
tech.root: wmformat
ms.assetid: a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3
ms.date: 12/05/2018
ms.keywords: IWMStatusCallback, IWMStatusCallback interface [windows Media Format], IWMStatusCallback interface [windows Media Format],described, IWMStatusCallbackInterface, wmformat.iwmstatuscallback, wmsdkidl/IWMStatusCallback
f1_keywords:
- wmsdkidl/IWMStatusCallback
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsdkidl.h
api_name:
- IWMStatusCallback
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStatusCallback interface


## -description



The <b>IWMStatusCallback</b> interface is implemented by the application to receive status information from various objects.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMStatusCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMStatusCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMStatusCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">OnStatus</a>
</td>
<td align="left" width="63%">
Called when status information must be communicated to the host application. This happens routinely when an ASF file is being opened and read, and when errors occur during reading.

</td>
</tr>
</table> 


## -remarks



The following methods and functions associate an implementation of this interface with an object:

<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing">IWMIndexer::StartIndexing</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicensebackup-backuplicenses">IWMLicenseBackup::BackupLicenses</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmlicenserestore-restorelicenses">IWMLicenseRestore::RestoreLicenses</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-open">IWMReader::Open</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise">IWMRegisterCallback::Advise</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer">WMCreateBackupRestorer</a>
</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback">IWMReaderCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

