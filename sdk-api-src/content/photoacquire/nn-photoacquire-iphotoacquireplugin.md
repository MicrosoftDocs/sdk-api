---
UID: NN:photoacquire.IPhotoAcquirePlugin
title: IPhotoAcquirePlugin (photoacquire.h)
description: Implement the IPhotoAcquirePlugin interface when you want to create a plug-in to run alongside the Windows Vista user interface (UI) for image acquisition. Registry settings are required to enable the plug-in.
old-location: picacq\iphotoacquireplugin.htm
tech.root: acquisition
ms.assetid: 7c8a0a49-8c15-4db2-8231-a48a3f76eb62
ms.date: 12/05/2018
ms.keywords: IPhotoAcquirePlugin, IPhotoAcquirePlugin interface [Picture Acquisition], IPhotoAcquirePlugin interface [Picture Acquisition],described, IPhotoAcquirePluginInterface, photoacquire/IPhotoAcquirePlugin, picacq.iphotoacquireplugin
ms.topic: interface
f1_keywords:
- photoacquire/IPhotoAcquirePlugin
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- photoacquire.h
api_name:
- IPhotoAcquirePlugin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPhotoAcquirePlugin interface


## -description



Implement the <code>IPhotoAcquirePlugin</code> interface when you want to create a plug-in to run alongside the Windows Vista user interface (UI) for image acquisition. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/register-the-plug-in">Registry settings</a> are required to enable the plug-in.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquirePlugin</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPhotoAcquirePlugin</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPhotoAcquirePlugin</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireplugin-displayconfiguredialog">DisplayConfigureDialog</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the configuration dialog is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireplugin-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the plug-in is initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireplugin-processitem">ProcessItem</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is transferred or enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/photoacquire/nf-photoacquire-iphotoacquireplugin-transfercomplete">TransferComplete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the transfer completes.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/acquisition/interfaces">Interfaces</a>
 

 

