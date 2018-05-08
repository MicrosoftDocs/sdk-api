---
UID: NN:photoacquire.IPhotoAcquirePlugin
title: IPhotoAcquirePlugin
author: windows-driver-content
description: Implement the IPhotoAcquirePlugin interface when you want to create a plug-in to run alongside the Windows Vista user interface (UI) for image acquisition. Registry settings are required to enable the plug-in.
old-location: picacq\iphotoacquireplugin.htm
old-project: acquisition
ms.assetid: 7c8a0a49-8c15-4db2-8231-a48a3f76eb62
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPhotoAcquirePlugin, IPhotoAcquirePlugin interface [Picture Acquisition], IPhotoAcquirePlugin interface [Picture Acquisition],described, IPhotoAcquirePluginInterface, photoacquire/IPhotoAcquirePlugin, picacq.iphotoacquireplugin
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: USER_INPUT_STRING_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	photoacquire.h
api_name:
-	IPhotoAcquirePlugin
product: Windows
targetos: Windows
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPhotoAcquirePlugin interface


## -description



Implement the <code>IPhotoAcquirePlugin</code> interface when you want to create a plug-in to run alongside the Windows Vista user interface (UI) for image acquisition. <a href="https://msdn.microsoft.com/18f36e53-11f0-469c-9790-9319a28ae2f2">Registry settings</a> are required to enable the plug-in.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPhotoAcquirePlugin</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPhotoAcquirePlugin</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/74257374-15c8-4e83-b271-2fd133f4dd7b">DisplayConfigureDialog</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the configuration dialog is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the plug-in is initialized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8a9144e-a728-48b7-a729-eec6d4db6d9e">ProcessItem</a>
</td>
<td align="left" width="63%">
Provides extended functionality each time a file is transferred or enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/915e676a-4aaa-4b10-b913-51b856c61dba">TransferComplete</a>
</td>
<td align="left" width="63%">
Provides extended functionality when the transfer completes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

