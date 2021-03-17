---
UID: NF:photoacquire.IPhotoAcquireOptionsDialog.Initialize
title: IPhotoAcquireOptionsDialog::Initialize (photoacquire.h)
description: Initializes the options dialog box and reads any saved options from the registry.
helpviewer_keywords: ["IPhotoAcquireOptionsDialog interface [Picture Acquisition]","Initialize method","IPhotoAcquireOptionsDialog.Initialize","IPhotoAcquireOptionsDialog::Initialize","IPhotoAcquireOptionsDialogInitialize","Initialize","Initialize method [Picture Acquisition]","Initialize method [Picture Acquisition]","IPhotoAcquireOptionsDialog interface","photoacquire/IPhotoAcquireOptionsDialog::Initialize","picacq.iphotoacquireoptionsdialog_initialize"]
old-location: picacq\iphotoacquireoptionsdialog_initialize.htm
tech.root: picacq
ms.assetid: 6e3c7876-28a6-4d5f-afca-7c0421df8c02
ms.date: 12/05/2018
ms.keywords: IPhotoAcquireOptionsDialog interface [Picture Acquisition],Initialize method, IPhotoAcquireOptionsDialog.Initialize, IPhotoAcquireOptionsDialog::Initialize, IPhotoAcquireOptionsDialogInitialize, Initialize, Initialize method [Picture Acquisition], Initialize method [Picture Acquisition],IPhotoAcquireOptionsDialog interface, photoacquire/IPhotoAcquireOptionsDialog::Initialize, picacq.iphotoacquireoptionsdialog_initialize
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
 - IPhotoAcquireOptionsDialog::Initialize
 - photoacquire/IPhotoAcquireOptionsDialog::Initialize
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
 - IPhotoAcquireOptionsDialog.Initialize
---

# IPhotoAcquireOptionsDialog::Initialize


## -description

Initializes the options dialog box and reads any saved options from the registry.

## -parameters

### -param pszRegistryRoot [in]

(optional) Pointer to a null-terminated string containing the registry root of a custom location to read the acquisition settings from. If this parameter is set to <b>NULL</b>, the default location will be used.

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

<code>Initialize</code> must be called prior to calling <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-create">Create</a> or <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireoptionsdialog-domodal">DoModal</a>. Failure to do so will cause <b>Create</b> or <b>DoModal</b> to fail.

If <code>Initialize</code> is called while the options dialog box is already displayed, an error will be returned.

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireoptionsdialog">IPhotoAcquireOptionsDialog Interface</a>