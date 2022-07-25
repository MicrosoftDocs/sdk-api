---
UID: NF:photoacquire.IPhotoAcquireSettings.SetSequencePaddingWidth
title: IPhotoAcquireSettings::SetSequencePaddingWidth (photoacquire.h)
description: The SetSequencePaddingWidth method sets a value indicating how wide sequential fields in filenames will be.
helpviewer_keywords: ["IPhotoAcquireSettings interface [Picture Acquisition]","SetSequencePaddingWidth method","IPhotoAcquireSettings.SetSequencePaddingWidth","IPhotoAcquireSettings::SetSequencePaddingWidth","IPhotoAcquireSettingsSetSequencePaddingWidth","SetSequencePaddingWidth","SetSequencePaddingWidth method [Picture Acquisition]","SetSequencePaddingWidth method [Picture Acquisition]","IPhotoAcquireSettings interface","photoacquire/IPhotoAcquireSettings::SetSequencePaddingWidth","picacq.iphotoacquiresettings_setsequencepaddingwidth"]
old-location: picacq\iphotoacquiresettings_setsequencepaddingwidth.htm
tech.root: picacq
ms.assetid: 2c90c109-1522-4722-a691-6f0f3caa50ec
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetSequencePaddingWidth method, IPhotoAcquireSettings.SetSequencePaddingWidth, IPhotoAcquireSettings::SetSequencePaddingWidth, IPhotoAcquireSettingsSetSequencePaddingWidth, SetSequencePaddingWidth, SetSequencePaddingWidth method [Picture Acquisition], SetSequencePaddingWidth method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetSequencePaddingWidth, picacq.iphotoacquiresettings_setsequencepaddingwidth
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
 - IPhotoAcquireSettings::SetSequencePaddingWidth
 - photoacquire/IPhotoAcquireSettings::SetSequencePaddingWidth
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
 - IPhotoAcquireSettings.SetSequencePaddingWidth
---

# IPhotoAcquireSettings::SetSequencePaddingWidth


## -description

The <code>SetSequencePaddingWidth</code> method sets a value indicating how wide sequential fields in filenames will be.

## -parameters

### -param dwWidth [in]

Double word value containing the width of sequential fields.

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

## -remarks

If the value passed to <code>SetSequencePaddingWidth</code> is nonzero and the format string specified in <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setoutputfilenametemplate">SetOutputFileNameTemplate</a> contains a sequential token, this method sets the width allotted for the sequential token. For example, given the template <code>$(GroupTag)$(AcquisitionSequence).$(OriginalExtension)</code>, if padding is set to 0, a file name might appear as 
``` syntax
"Image1.jpg"
```
 If padding is set to 3, the file name may appear as 
``` syntax
"Image   1.jpg"
```


## -see-also

<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-getsequencepaddingwidth">GetSequencePaddingWidth</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresettings">IPhotoAcquireSettings Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquiresettings-setsequencezeropadding">SetSequenceZeroPadding</a>
