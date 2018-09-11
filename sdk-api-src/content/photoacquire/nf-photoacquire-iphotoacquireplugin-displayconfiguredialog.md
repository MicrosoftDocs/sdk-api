---
UID: NF:photoacquire.IPhotoAcquirePlugin.DisplayConfigureDialog
title: IPhotoAcquirePlugin::DisplayConfigureDialog
author: windows-sdk-content
description: The DisplayConfigureDialog method provides extended functionality when the configuration dialog is displayed. The application provides the implementation of the DisplayConfigureDialog method.
old-location: picacq\iphotoacquireplugin_displayconfiguredialog.htm
tech.root: acquisition
ms.assetid: 74257374-15c8-4e83-b271-2fd133f4dd7b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: DisplayConfigureDialog, DisplayConfigureDialog method [Picture Acquisition], DisplayConfigureDialog method [Picture Acquisition],IPhotoAcquirePlugin interface, IPhotoAcquirePlugin interface [Picture Acquisition],DisplayConfigureDialog method, IPhotoAcquirePlugin.DisplayConfigureDialog, IPhotoAcquirePlugin::DisplayConfigureDialog, IPhotoAcquirePluginDisplayConfigureDialog, photoacquire/IPhotoAcquirePlugin::DisplayConfigureDialog, picacq.iphotoacquireplugin_displayconfiguredialog
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/7c8a0a49-8c15-4db2-8231-a48a3f76eb62">IPhotoAcquirePlugin Interface</a>
 

 

