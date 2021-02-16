---
UID: NF:photoacquire.IPhotoAcquirePlugin.TransferComplete
title: IPhotoAcquirePlugin::TransferComplete (photoacquire.h)
description: Provides extended functionality when a transfer session is completed. The application provides the implementation of the TransferComplete method.
helpviewer_keywords: ["IPhotoAcquirePlugin interface [Picture Acquisition]","TransferComplete method","IPhotoAcquirePlugin.TransferComplete","IPhotoAcquirePlugin::TransferComplete","IPhotoAcquirePluginTransferComplete","TransferComplete","TransferComplete method [Picture Acquisition]","TransferComplete method [Picture Acquisition]","IPhotoAcquirePlugin interface","photoacquire/IPhotoAcquirePlugin::TransferComplete","picacq.iphotoacquireplugin_transfercomplete"]
old-location: picacq\iphotoacquireplugin_transfercomplete.htm
tech.root: picacq
ms.assetid: 915e676a-4aaa-4b10-b913-51b856c61dba
ms.date: 12/05/2018
ms.keywords: IPhotoAcquirePlugin interface [Picture Acquisition],TransferComplete method, IPhotoAcquirePlugin.TransferComplete, IPhotoAcquirePlugin::TransferComplete, IPhotoAcquirePluginTransferComplete, TransferComplete, TransferComplete method [Picture Acquisition], TransferComplete method [Picture Acquisition],IPhotoAcquirePlugin interface, photoacquire/IPhotoAcquirePlugin::TransferComplete, picacq.iphotoacquireplugin_transfercomplete
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
 - IPhotoAcquirePlugin::TransferComplete
 - photoacquire/IPhotoAcquirePlugin::TransferComplete
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
 - IPhotoAcquirePlugin.TransferComplete
---

# IPhotoAcquirePlugin::TransferComplete


## -description

Provides extended functionality when a transfer session is completed. The application provides the implementation of the <b>TransferComplete</b> method.

## -parameters

### -param hr [in]

Specifies the result of the transfer operation.

## -returns

The method returns an <b>HRESULT</b>. Your implementation is not limited to the following return values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireplugin">IPhotoAcquirePlugin Interface</a>