---
UID: NN:wia_lh.IWiaTransferCallback
title: IWiaTransferCallback
author: windows-driver-content
description: The IWiaTransferCallback interface is implemented by image processing filter developers and called by Microsoft Windows Image Acquisition (WIA).
old-location: image\iwiatransfercallback_interface.htm
old-project: image
ms.assetid: c85e5faa-b14b-4775-a5cc-cec5e20dc974
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaTransferCallback, IWiaTransferCallback interface [Imaging Devices], IWiaTransferCallback interface [Imaging Devices], described, IWiaTransfercallback_ae8874d9-135f-4627-bbec-51cebd6c3d69.xml, image.iwiatransfercallback_interface, wia_lh/IWiaTransferCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wia_lh.h
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wia_lh.h
api_name:
-	IWiaTransferCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaTransferCallback interface


## -description


The <b>IWiaTransferCallback</b> interface is implemented by image processing filter developers and called by Microsoft Windows Image Acquisition (WIA).

This interface's methods are called as a result of an application calling <b>IWiaTransfer::Download</b> or the preview component's <b>IWiaPreview::GetNewPreview</b>.

This interface is available in Windows Vista and later operating system versions.

The methods on this interface depend on the <b>IWiaTransfer</b> and <b>IWiaPreview</b> interfaces, both of which are described in the Microsoft Windows SDK documentation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaTransferCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaTransferCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaTransferCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj151551">GetNextStream</a>
</td>
<td align="left" width="63%">
The <b>IWiaTransferCallback::GetNextStream</b> method is implemented by an image processing filter. It is called by the WIA service as a result of an application calling <b>IWiaTransfer::Download</b> or the preview component's <b>IWiaPreview::GetNewPreview</b>. The <b>IWiaTransfer</b> and <b>IWiaPreview</b> interfaces are described in the Microsoft Windows SDK documentation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc6c2057-9617-4c69-ac79-2a8f910a1ee2">TransferCallback</a>
</td>
<td align="left" width="63%">
The <b>IWiaTransferCallback::TransferCallback</b> method is implemented by an image processing filter. It is called by the WIA service as a result of an application calling <b>IWiaTransfer::Download</b> or the preview component's <b>IWiaPreview::GetNewPreview</b>.

</td>
</tr>
</table> 

