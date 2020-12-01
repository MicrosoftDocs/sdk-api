---
UID: NF:imapi2fs.IBootOptions.get_PlatformId
title: IBootOptions::get_PlatformId (imapi2fs.h)
description: Retrieves the platform identifier that identifies the operating system architecture that the boot image supports.
helpviewer_keywords: ["IBootOptions interface [IMAPI]","get_PlatformId method","IBootOptions.get_PlatformId","IBootOptions::get_PlatformId","get_PlatformId","get_PlatformId method [IMAPI]","get_PlatformId method [IMAPI]","IBootOptions interface","imapi.ibootoptions_get_platformid","imapi2fs/IBootOptions::get_PlatformId"]
old-location: imapi\ibootoptions_get_platformid.htm
tech.root: imapi
ms.assetid: 8d5ceb0e-4fd2-4146-8e15-b157c80a9d5b
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],get_PlatformId method, IBootOptions.get_PlatformId, IBootOptions::get_PlatformId, get_PlatformId, get_PlatformId method [IMAPI], get_PlatformId method [IMAPI],IBootOptions interface, imapi.ibootoptions_get_platformid, imapi2fs/IBootOptions::get_PlatformId
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
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
 - IBootOptions::get_PlatformId
 - imapi2fs/IBootOptions::get_PlatformId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IBootOptions.get_PlatformId
---

# IBootOptions::get_PlatformId


## -description

Retrieves the platform identifier that identifies the operating system architecture that the boot image supports.

## -parameters

### -param pVal [out]

Identifies the operating system architecture that the boot image supports. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-platformid">PlatformId</a> enumeration type.

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

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-put_platformid">IBootOptions::put_PlatformId</a>