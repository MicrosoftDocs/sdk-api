---
UID: NN:wiamindr_lh.IWiaMiniDrvTransferCallback
title: IWiaMiniDrvTransferCallback
author: windows-driver-content
description: This is a Callback interface that is called by the WIA mini-driver for stream-based transfers.
old-location: image\iwiaminidrvtransfercallback.htm
old-project: image
ms.assetid: A3D874CB-1F43-4AA0-975B-35C0C5F7A13C
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: IWiaMiniDrvTransferCallback, IWiaMiniDrvTransferCallback interface [Imaging Devices], IWiaMiniDrvTransferCallback interface [Imaging Devices], described, image.iwiaminidrvtransfercallback, wiamindr_lh/IWiaMiniDrvTransferCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wiamindr_lh.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
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
req.typenames: SCANWINDOW, *PSCANWINDOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiamindr_lh.h
api_name:
-	IWiaMiniDrvTransferCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrvTransferCallback interface


## -description


This is a Callback interface that is called by the WIA mini-driver for stream-based transfers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWiaMiniDrvTransferCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWiaMiniDrvTransferCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWiaMiniDrvTransferCallback</b> interface has these methods.
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
Called by the WIA mini-driver to obtain a stream for the current data transfer (download or upload).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj151552">SendMessage</a>
</td>
<td align="left" width="63%">
Periodically called by the WIA mini-driver during a data transfer, to update the WIA application client about the progress and status of the transfer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0cdc02bf-23fe-4122-8d5f-f42c3c07da8b">Cancellation of Data Transfers in Windows Vista</a>



<a href="https://msdn.microsoft.com/83817277-3526-4f64-8e7c-7e02c8cd77bd">Data Transfer Between Legacy Application and Windows Vista Driver</a>



<a href="https://msdn.microsoft.com/fb830522-f95e-4dd7-8c1b-de092a6c5a51">IStream Transfer Driver Example</a>



<a href="http://msdn.microsoft.com/windows/hardware/gg463512">Introduction to WIA 2.0</a>
 

 

