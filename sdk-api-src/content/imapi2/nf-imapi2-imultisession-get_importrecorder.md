---
UID: NF:imapi2.IMultisession.get_ImportRecorder
title: IMultisession::get_ImportRecorder (imapi2.h)
description: Retrieves the disc recorder to use to import one or more previous sessions.
helpviewer_keywords: ["IMultisession interface [IMAPI]","get_ImportRecorder method","IMultisession.get_ImportRecorder","IMultisession::get_ImportRecorder","get_ImportRecorder","get_ImportRecorder method [IMAPI]","get_ImportRecorder method [IMAPI]","IMultisession interface","imapi.imultisession_get_importrecorder","imapi2/IMultisession::get_ImportRecorder"]
old-location: imapi\imultisession_get_importrecorder.htm
tech.root: imapi
ms.assetid: eca127eb-0e0a-4f43-afa4-42fde8d43284
ms.date: 12/05/2018
ms.keywords: IMultisession interface [IMAPI],get_ImportRecorder method, IMultisession.get_ImportRecorder, IMultisession::get_ImportRecorder, get_ImportRecorder, get_ImportRecorder method [IMAPI], get_ImportRecorder method [IMAPI],IMultisession interface, imapi.imultisession_get_importrecorder, imapi2/IMultisession::get_ImportRecorder
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IMultisession::get_ImportRecorder
 - imapi2/IMultisession::get_ImportRecorder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IMultisession.get_ImportRecorder
---

# IMultisession::get_ImportRecorder


## -description

Retrieves the disc recorder to use to import one or more previous sessions.

## -parameters

### -param value [out]

An <a href="/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2">IDiscRecorder2</a> interface that identifies the device that contains one or more session images to import.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -remarks

The import recorder reads session content from the optical media and provides it to <a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage">IFileSystemImage</a>.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>