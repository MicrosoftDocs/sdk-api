---
UID: NF:wiamindr_lh.IWiaMiniDrvTransferCallback.GetNextStream
title: IWiaMiniDrvTransferCallback::GetNextStream method
author: windows-driver-content
description: Called by the WIA mini-driver to obtain a stream for the current data transfer (download or upload).
old-location: image\iwiaminidrvtransfercallback_getnextstream.htm
old-project: image
ms.assetid: FF33471A-692B-4568-BF37-1870DEC367D0
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: GetNextStream method [Imaging Devices], GetNextStream method [Imaging Devices], IWiaMiniDrvTransferCallback interface, GetNextStream,IWiaMiniDrvTransferCallback.GetNextStream, IWiaMiniDrvTransferCallback, IWiaMiniDrvTransferCallback interface [Imaging Devices], GetNextStream method, IWiaMiniDrvTransferCallback::GetNextStream, image.iwiaminidrvtransfercallback_getnextstream, wiamindr_lh/IWiaMiniDrvTransferCallback::GetNextStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	IWiaMiniDrvTransferCallback.GetNextStream
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrvTransferCallback::GetNextStream method


## -description


Called by the WIA mini-driver to obtain a stream for the current data transfer (download or upload).


## -parameters




### -param lFlags [in]

Represents flag bits. This parameter is unused and should always be set to zero (0) by the caller.


### -param bstrItemName [in]

The name of the item that will perform the data transfer. For more information, see  <a href="https://msdn.microsoft.com/library/windows/hardware/ff551590">WIA_IPA_ITEM_NAME</a>.


### -param bstrFullItemName [in]

The full name of the item that will perform the data transfer. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff551561">WIA_IPA_FULL_ITEM_NAME</a>.


### -param ppIStream [out]

A pointer to an <b>IStream</b> object.


## -returns



This method returns S_OK when the call is successful. Otherwise it returns an appropriate HRESULT error code.




## -remarks



When the client requests to skip the data transfer, the <b>GetNextStream</b> method returns WIA_STATUS_SKIP_ITEM. The WIA mini-driver must skip the current image transfer and continue with the next image transfer, if any. For example, for a download transfer, finish scanning the current image and then discard the image data.

When the current transfer sequence is cancelled, the <b>GetNextStream</b> method returns S_FALSE.




## -see-also




<a href="https://msdn.microsoft.com/0cdc02bf-23fe-4122-8d5f-f42c3c07da8b">Cancellation of Data Transfers in Windows Vista</a>



<a href="https://msdn.microsoft.com/83817277-3526-4f64-8e7c-7e02c8cd77bd">Data Transfer Between Legacy Application and Windows Vista Driver</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj151550">IWiaMiniDrvTransferCallback</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551561">WIA_IPA_FULL_ITEM_NAME</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551590">WIA_IPA_ITEM_NAME</a>
 

 

