---
UID: NF:imapi.IDiscRecorder.GetPath
title: IDiscRecorder::GetPath (imapi.h)
description: Retrieves a path to the device within the operating system. This path should be used in conjunction with the display name to completely identify an available disc recorder.
helpviewer_keywords: ["GetPath","GetPath method [IMAPI]","GetPath method [IMAPI]","IDiscRecorder interface","IDiscRecorder interface [IMAPI]","GetPath method","IDiscRecorder.GetPath","IDiscRecorder::GetPath","_win32_idiscrecorder_getpath","base.idiscrecorder_getpath","imapi.idiscrecorder_getpath","imapi/IDiscRecorder::GetPath"]
old-location: imapi\idiscrecorder_getpath.htm
tech.root: imapi
ms.assetid: bceb7302-e5e6-4ee5-9adb-1736ab62e819
ms.date: 12/05/2018
ms.keywords: GetPath, GetPath method [IMAPI], GetPath method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],GetPath method, IDiscRecorder.GetPath, IDiscRecorder::GetPath, _win32_idiscrecorder_getpath, base.idiscrecorder_getpath, imapi.idiscrecorder_getpath, imapi/IDiscRecorder::GetPath
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
 - IDiscRecorder::GetPath
 - imapi/IDiscRecorder::GetPath
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
 - IDiscRecorder.GetPath
---

# IDiscRecorder::GetPath


## -description

Retrieves a path to the device within the operating system. This path should be used in conjunction with the display name to completely identify an available disc recorder.

## -parameters

### -param pbstrPath [out]

Path to the disc recorder. This path may be of the form \Device\CdRom<i>X</i>, but you should not rely on the path following this convention.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

## -see-also

<a href="/windows/desktop/api/imapi/nn-imapi-idiscrecorder">IDiscRecorder</a>