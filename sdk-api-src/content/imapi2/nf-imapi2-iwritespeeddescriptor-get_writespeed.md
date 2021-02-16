---
UID: NF:imapi2.IWriteSpeedDescriptor.get_WriteSpeed
title: IWriteSpeedDescriptor::get_WriteSpeed (imapi2.h)
description: Retrieves the supported write speed for writing to the media.
helpviewer_keywords: ["IWriteSpeedDescriptor interface [IMAPI]","get_WriteSpeed method","IWriteSpeedDescriptor.get_WriteSpeed","IWriteSpeedDescriptor::get_WriteSpeed","get_WriteSpeed","get_WriteSpeed method [IMAPI]","get_WriteSpeed method [IMAPI]","IWriteSpeedDescriptor interface","imapi.iwritespeeddescriptor_get_writespeed","imapi2/IWriteSpeedDescriptor::get_WriteSpeed"]
old-location: imapi\iwritespeeddescriptor_get_writespeed.htm
tech.root: imapi
ms.assetid: 9136a735-d902-48bc-bddd-297c1e32310e
ms.date: 12/05/2018
ms.keywords: IWriteSpeedDescriptor interface [IMAPI],get_WriteSpeed method, IWriteSpeedDescriptor.get_WriteSpeed, IWriteSpeedDescriptor::get_WriteSpeed, get_WriteSpeed, get_WriteSpeed method [IMAPI], get_WriteSpeed method [IMAPI],IWriteSpeedDescriptor interface, imapi.iwritespeeddescriptor_get_writespeed, imapi2/IWriteSpeedDescriptor::get_WriteSpeed
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
 - IWriteSpeedDescriptor::get_WriteSpeed
 - imapi2/IWriteSpeedDescriptor::get_WriteSpeed
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
 - IWriteSpeedDescriptor.get_WriteSpeed
---

# IWriteSpeedDescriptor::get_WriteSpeed


## -description

Retrieves the supported write speed for writing to the media.

## -parameters

### -param value [out]

Write speed of the current media, measured in sectors per second.

## -returns

S_OK   is typically returned on success, but the return of other success values is possible.  The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

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

The write speed is based on the media write speeds. The value of this property can change when a media change occurs.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-iwritespeeddescriptor">IWriteSpeedDescriptor</a>