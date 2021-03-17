---
UID: NF:photoacquire.IPhotoAcquirePlugin.ProcessItem
title: IPhotoAcquirePlugin::ProcessItem (photoacquire.h)
description: The ProcessItem method provides additional functionality each time an item is processed. The application provides the implementation of the ProcessItem method.
helpviewer_keywords: ["IPhotoAcquirePlugin interface [Picture Acquisition]","ProcessItem method","IPhotoAcquirePlugin.ProcessItem","IPhotoAcquirePlugin::ProcessItem","IPhotoAcquirePluginProcessItem","ProcessItem","ProcessItem method [Picture Acquisition]","ProcessItem method [Picture Acquisition]","IPhotoAcquirePlugin interface","photoacquire/IPhotoAcquirePlugin::ProcessItem","picacq.iphotoacquireplugin_processitem"]
old-location: picacq\iphotoacquireplugin_processitem.htm
tech.root: picacq
ms.assetid: f8a9144e-a728-48b7-a729-eec6d4db6d9e
ms.date: 12/05/2018
ms.keywords: IPhotoAcquirePlugin interface [Picture Acquisition],ProcessItem method, IPhotoAcquirePlugin.ProcessItem, IPhotoAcquirePlugin::ProcessItem, IPhotoAcquirePluginProcessItem, ProcessItem, ProcessItem method [Picture Acquisition], ProcessItem method [Picture Acquisition],IPhotoAcquirePlugin interface, photoacquire/IPhotoAcquirePlugin::ProcessItem, picacq.iphotoacquireplugin_processitem
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
 - IPhotoAcquirePlugin::ProcessItem
 - photoacquire/IPhotoAcquirePlugin::ProcessItem
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
 - IPhotoAcquirePlugin.ProcessItem
---

# IPhotoAcquirePlugin::ProcessItem


## -description

The <code>ProcessItem</code> method provides additional functionality each time an item is processed. The application provides the implementation of the <code>ProcessItem</code> method.

## -parameters

### -param dwAcquireStage [in]

Specifies a double word value indicating whether this method is being called before or after processing an item. Must be one of: PAPS_PRESAVE, PAPS_POSTSAVE, or PAPS_CLEANUP.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>PAPS_PRESAVE</td>
<td>Indicates that the method is being called before saving the acquired file. During PAPS_PRESAVE, <a href="/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireitem-getproperty">pPhotoAcquireItem::GetProperty</a> should be used to retrieve metadata from the original file, while new metadata to be written to the file should be added to <i>pPropertyStore</i>.</td>
</tr>
<tr>
<td>PAPS_POSTSAVE</td>
<td>Indicates that the method is being called after saving the acquired file.</td>
</tr>
<tr>
<td>PAPS_CLEANUP</td>
<td>Indicates that the user has canceled the acquire operation and any work done by the plug-in should be cleaned up.</td>
</tr>
</table>

### -param pPhotoAcquireItem [in]

Pointer to an <a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireitem">IPhotoAcquireItem</a> object for the item being processed.

### -param pOriginalItemStream [in]

Pointer to an <b>IStream</b> object for the original item. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_POSTSAVE.

### -param pszFinalFilename [in]

The file name of the destination of the item. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_PRESAVE.

### -param pPropertyStore [in]

The item's property store. <b>NULL</b> if <i>dwAcquireStage</i> is PAPS_POSTSAVE.

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
The method is not implemented.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/photoacquire/nn-photoacquire-iphotoacquireplugin">IPhotoAcquirePlugin Interface</a>