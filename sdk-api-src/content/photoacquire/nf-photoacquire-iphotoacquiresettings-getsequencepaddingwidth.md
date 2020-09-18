---
UID: NF:photoacquire.IPhotoAcquireSettings.GetSequencePaddingWidth
title: IPhotoAcquireSettings::GetSequencePaddingWidth (photoacquire.h)
description: The GetSequencePaddingWidth method retrieves a value indicating how wide sequential fields in file names will be.
helpviewer_keywords: ["GetSequencePaddingWidth","GetSequencePaddingWidth method [Picture Acquisition]","GetSequencePaddingWidth method [Picture Acquisition]","IPhotoAcquireSettings interface","IPhotoAcquireSettings interface [Picture Acquisition]","GetSequencePaddingWidth method","IPhotoAcquireSettings.GetSequencePaddingWidth","IPhotoAcquireSettings::GetSequencePaddingWidth","IPhotoAcquireSettingsGetSequencePaddingWidth","photoacquire/IPhotoAcquireSettings::GetSequencePaddingWidth","picacq.iphotoacquiresettings_getsequencepaddingwidth"]
old-location: picacq\iphotoacquiresettings_getsequencepaddingwidth.htm
tech.root: picacq
ms.assetid: d19a103e-0f5a-493d-a515-21d8730e39e3
ms.date: 12/05/2018
ms.keywords: GetSequencePaddingWidth, GetSequencePaddingWidth method [Picture Acquisition], GetSequencePaddingWidth method [Picture Acquisition],IPhotoAcquireSettings interface, IPhotoAcquireSettings interface [Picture Acquisition],GetSequencePaddingWidth method, IPhotoAcquireSettings.GetSequencePaddingWidth, IPhotoAcquireSettings::GetSequencePaddingWidth, IPhotoAcquireSettingsGetSequencePaddingWidth, photoacquire/IPhotoAcquireSettings::GetSequencePaddingWidth, picacq.iphotoacquiresettings_getsequencepaddingwidth
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
 - IPhotoAcquireSettings::GetSequencePaddingWidth
 - photoacquire/IPhotoAcquireSettings::GetSequencePaddingWidth
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
 - IPhotoAcquireSettings.GetSequencePaddingWidth
---

# IPhotoAcquireSettings::GetSequencePaddingWidth


## -description

The <code>GetSequencePaddingWidth</code> method retrieves a value indicating how wide sequential fields in file names will be.

## -parameters

### -param pdwWidth [out]

Pointer to a double word value containing the width of sequential fields.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A non-NULL value was expected.

</td>
</tr>
</table>

## -remarks

If the format string specified in <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setoutputfilenametemplate">SetOutputFileNameTemplate</a> contains a sequential token, this method gets the width allotted for the sequential token.

If the format string does not contain a sequential token, the value returned by this method is not defined.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencepaddingwidth">SetSequencePaddingWidth</a>