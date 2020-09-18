---
UID: NF:photoacquire.IPhotoAcquirePlugin.Initialize
title: IPhotoAcquirePlugin::Initialize (photoacquire.h)
description: The Initialize method provides extended functionality when the plug-in is initialized. The application provides the implementation of the Initialize method.
helpviewer_keywords: ["IPhotoAcquirePlugin interface [Picture Acquisition]","Initialize method","IPhotoAcquirePlugin.Initialize","IPhotoAcquirePlugin::Initialize","IPhotoAcquirePluginInitialize","Initialize","Initialize method [Picture Acquisition]","Initialize method [Picture Acquisition]","IPhotoAcquirePlugin interface","photoacquire/IPhotoAcquirePlugin::Initialize","picacq.iphotoacquireplugin_initialize"]
old-location: picacq\iphotoacquireplugin_initialize.htm
tech.root: picacq
ms.assetid: 0992e4f0-43a0-49fb-99f4-8713af96ef7e
ms.date: 12/05/2018
ms.keywords: IPhotoAcquirePlugin interface [Picture Acquisition],Initialize method, IPhotoAcquirePlugin.Initialize, IPhotoAcquirePlugin::Initialize, IPhotoAcquirePluginInitialize, Initialize, Initialize method [Picture Acquisition], Initialize method [Picture Acquisition],IPhotoAcquirePlugin interface, photoacquire/IPhotoAcquirePlugin::Initialize, picacq.iphotoacquireplugin_initialize
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
 - IPhotoAcquirePlugin::Initialize
 - photoacquire/IPhotoAcquirePlugin::Initialize
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
 - IPhotoAcquirePlugin.Initialize
---

# IPhotoAcquirePlugin::Initialize


## -description

The <code>Initialize</code> method provides extended functionality when the plug-in is initialized. The application provides the implementation of the <code>Initialize</code> method.

## -parameters

### -param pPhotoAcquireSource [in]

Specifies the source from which photos are being acquired.

### -param pPhotoAcquireProgressCB [in]

Specifies the callback that will provide additional processing during acquisition.

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



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireprogresscb">IPhotoAcquireProgressCB Interface</a>



<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquiresource">IPhotoAcquireSource Interface</a>