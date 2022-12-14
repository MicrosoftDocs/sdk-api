---
UID: NF:imapi.IDiscRecorder.OpenExclusive
title: IDiscRecorder::OpenExclusive (imapi.h)
description: Opens a disc recorder for exclusive access.
helpviewer_keywords: ["IDiscRecorder interface [IMAPI]","OpenExclusive method","IDiscRecorder.OpenExclusive","IDiscRecorder::OpenExclusive","OpenExclusive","OpenExclusive method [IMAPI]","OpenExclusive method [IMAPI]","IDiscRecorder interface","_win32_idiscrecorder_openexclusive","base.idiscrecorder_openexclusive","imapi.idiscrecorder_openexclusive","imapi/IDiscRecorder::OpenExclusive"]
old-location: imapi\idiscrecorder_openexclusive.htm
tech.root: imapi
ms.assetid: e704baf0-d403-4cf7-aa32-16677d9a8694
ms.date: 12/05/2018
ms.keywords: IDiscRecorder interface [IMAPI],OpenExclusive method, IDiscRecorder.OpenExclusive, IDiscRecorder::OpenExclusive, OpenExclusive, OpenExclusive method [IMAPI], OpenExclusive method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_openexclusive, base.idiscrecorder_openexclusive, imapi.idiscrecorder_openexclusive, imapi/IDiscRecorder::OpenExclusive
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDiscRecorder::OpenExclusive
 - imapi/IDiscRecorder::OpenExclusive
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder.OpenExclusive
---

# IDiscRecorder::OpenExclusive


## -description

Opens a disc recorder for exclusive access.



## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -remarks

This method blocks file system access to a recorder through applications such as Explorer. The recorder must be opened with this method before it is possible to use the following methods: 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-querymediatype">QueryMediaType</a>, 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-eject">Eject</a>, 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-erase">Erase</a>, and 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-close">Close</a>.

It is important to close the recorder before calling 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscmaster-recorddisc">IDiscMaster::RecordDisc</a>, or it will fail with IMAPI_E_DEVICE_NOTACCESSIBLE. The device is exclusively committed to access through either 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a> or 
<a href="/windows/desktop/api/imapi/nn-imapi-idiscmaster">IDiscMaster</a>, but not both at the same time. This is to ensure that there is no confusion regarding allowed operations and ownership of a recorder during application control or a burn.

An exclusive lock should be held for as short a time as possible. Requests that come from other operating system components are not queued for later execution. Instead, they are simply failed. This could cause confusion with users who don't think a burn is in progress.

Any time that 
<b>OpenExclusive</b> is called, it appears to the file system that the disc has been removed. When the corresponding 
<a href="/windows/desktop/api/imapi/nf-imapi-idiscrecorder-close">Close</a> call is made, it appears to the file system that the media has reappeared. This may cause auto-run issues.

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>
