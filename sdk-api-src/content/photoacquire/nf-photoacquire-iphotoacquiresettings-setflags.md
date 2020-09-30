---
UID: NF:photoacquire.IPhotoAcquireSettings.SetFlags
title: IPhotoAcquireSettings::SetFlags (photoacquire.h)
description: The SetFlags method sets the photo acquire flags.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","SetFlags method","IPhotoAcquireSettings.SetFlags","IPhotoAcquireSettings::SetFlags","IPhotoAcquireSettingsSetFlags","SetFlags","SetFlags method [Picture Acquisition]","SetFlags method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::SetFlags","picacq.iphotoacquiresettings_setflags"]
old-location: picacq\iphotoacquiresettings_setflags.htm
tech.root: picacq
ms.assetid: aebe06d8-c764-4d2d-9bd2-58fd9e3714bd
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetFlags method, IPhotoAcquireSettings.SetFlags, IPhotoAcquireSettings::SetFlags, IPhotoAcquireSettingsSetFlags, SetFlags, SetFlags method [Picture Acquisition], SetFlags method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetFlags, picacq.iphotoacquiresettings_setflags
req.header: photoacquire.h
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
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPhotoAcquireSettings::SetFlags
 - photoacquire/IPhotoAcquireSettings::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSettings.SetFlags
---

# IPhotoAcquireSettings::SetFlags


## -description

The <code>SetFlags</code> method sets the photo acquire flags.

## -parameters

### -param dwPhotoAcquireFlags [in]

Double word value containing the photo acquire flags.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getflags">GetFlags</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>