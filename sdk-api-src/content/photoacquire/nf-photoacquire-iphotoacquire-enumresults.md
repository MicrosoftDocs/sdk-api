---
UID: NF:photoacquire.IPhotoAcquire.EnumResults
title: IPhotoAcquire::EnumResults (photoacquire.h)
description: The EnumResults method retrieves an enumeration containing the paths of all files successfully transferred during the most recent call to Acquire.
helpviewer_keywords: ["EnumResults","EnumResults method [Picture Acquisition]","EnumResults method [Picture Acquisition]","IPhotoAcquire interface","IPhotoAcquire interface [Picture Acquisition]","EnumResults method","IPhotoAcquire.EnumResults","IPhotoAcquire::EnumResults","IPhotoAcquireEnumResults","photoacquire/IPhotoAcquire::EnumResults","picacq.iphotoacquire_enumresults"]
old-location: picacq\iphotoacquire_enumresults.htm
tech.root: picacq
ms.assetid: 2f3bd36c-3daf-4738-8240-ce622d988861
ms.date: 12/05/2018
ms.keywords: EnumResults, EnumResults method [Picture Acquisition], EnumResults method [Picture Acquisition],IPhotoAcquire interface, IPhotoAcquire interface [Picture Acquisition],EnumResults method, IPhotoAcquire.EnumResults, IPhotoAcquire::EnumResults, IPhotoAcquireEnumResults, photoacquire/IPhotoAcquire::EnumResults, picacq.iphotoacquire_enumresults
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
 - IPhotoAcquire::EnumResults
 - photoacquire/IPhotoAcquire::EnumResults
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
 - IPhotoAcquire.EnumResults
---

# IPhotoAcquire::EnumResults


## -description

The <code>EnumResults</code> method retrieves an enumeration containing the paths of all files successfully transferred during the most recent call to <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">Acquire</a>.

## -parameters

### -param ppEnumFilePaths [out]

Returns an enumeration containing the paths to all the transferred files.

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
A non-<b>NULL</b> pointer was expected.

</td>
</tr>
</table>

## -remarks

If the file transfer is aborted before any files are transferred, <i>ppEnumFilePaths</i> will be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquire">IPhotoAcquire Interface</a>



<a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquire-acquire">IPhotoAcquire::Acquire</a>