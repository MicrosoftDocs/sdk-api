---
UID: NF:photoacquire.IPhotoAcquirePlugin.DisplayConfigureDialog
title: IPhotoAcquirePlugin::DisplayConfigureDialog (photoacquire.h)
description: The DisplayConfigureDialog method provides extended functionality when the configuration dialog is displayed. The application provides the implementation of the DisplayConfigureDialog method.
helpviewer_keywords: ["DisplayConfigureDialog","DisplayConfigureDialog method [Picture Acquisition]","DisplayConfigureDialog method [Picture Acquisition]","IPhotoAcquirePlugin interface","IPhotoAcquirePlugin interface [Picture Acquisition]","DisplayConfigureDialog method","IPhotoAcquirePlugin.DisplayConfigureDialog","IPhotoAcquirePlugin::DisplayConfigureDialog","IPhotoAcquirePluginDisplayConfigureDialog","photoacquire/IPhotoAcquirePlugin::DisplayConfigureDialog","picacq.iphotoacquireplugin_displayconfiguredialog"]
old-location: picacq\iphotoacquireplugin_displayconfiguredialog.htm
tech.root: picacq
ms.assetid: 74257374-15c8-4e83-b271-2fd133f4dd7b
ms.date: 12/05/2018
ms.keywords: DisplayConfigureDialog, DisplayConfigureDialog method [Picture Acquisition], DisplayConfigureDialog method [Picture Acquisition],IPhotoAcquirePlugin interface, IPhotoAcquirePlugin interface [Picture Acquisition],DisplayConfigureDialog method, IPhotoAcquirePlugin.DisplayConfigureDialog, IPhotoAcquirePlugin::DisplayConfigureDialog, IPhotoAcquirePluginDisplayConfigureDialog, photoacquire/IPhotoAcquirePlugin::DisplayConfigureDialog, picacq.iphotoacquireplugin_displayconfiguredialog
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
 - IPhotoAcquirePlugin::DisplayConfigureDialog
 - photoacquire/IPhotoAcquirePlugin::DisplayConfigureDialog
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
 - IPhotoAcquirePlugin.DisplayConfigureDialog
---

# IPhotoAcquirePlugin::DisplayConfigureDialog


## -description

The <code>DisplayConfigureDialog</code> method provides extended functionality when the configuration dialog is displayed. The application provides the implementation of the <code>DisplayConfigureDialog</code> method.

## -parameters

### -param hWndParent [in]

Specifies the handle to the configuration dialog window.

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