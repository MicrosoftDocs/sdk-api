---
UID: NF:wiamindr_lh.IWiaMiniDrvCallBack.MiniDrvCallback
title: IWiaMiniDrvCallBack::MiniDrvCallback method
author: windows-driver-content
description: The MiniDrvCallback method provides a callback method for WIA minidrivers to use during a callback data transfer.
old-location: image\iwiaminidrvcallback_minidrvcallback.htm
old-project: image
ms.assetid: 7d1c0d8a-65db-47fd-ad6a-a83c7ed3acd9
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CallBack_ab4a8e02-c505-49d4-8933-27428333a00d.xml, IWiaMiniDrvCallBack, IWiaMiniDrvCallBack interface [Imaging Devices], MiniDrvCallback method, IWiaMiniDrvCallBack::MiniDrvCallback, MiniDrvCallback method [Imaging Devices], MiniDrvCallback method [Imaging Devices], IWiaMiniDrvCallBack interface, MiniDrvCallback,IWiaMiniDrvCallBack.MiniDrvCallback, image.iwiaminidrvcallback_minidrvcallback, wiamindr_lh/IWiaMiniDrvCallBack::MiniDrvCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamindr_lh.h
req.include-header: Wiamindr.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later.
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
-	wiamindr_lh.h
api_name:
-	IWiaMiniDrvCallBack.MiniDrvCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaMiniDrvCallBack::MiniDrvCallback method


## -description


The <b>MiniDrvCallback</b> method provides a callback method for WIA minidrivers to use during a callback data transfer.


## -parameters




### -param lReason [in]

Specifies a constant value that designates a callback status message. This value is used to determine the purpose of the callback, and can be one of the following values:

<table>
<tr>
<th>Message</th>
<th>Definition</th>
</tr>
<tr>
<td>
IT_MSG_DATA

</td>
<td>
Indicates that the transfer buffer contains a block of data.

</td>
</tr>
<tr>
<td>
IT_MSG_DATA_HEADER

</td>
<td>
Received before any data transfers. Indicates that the transfer buffer points to a WIA_DATA_CALLBACK_HEADER structure (defined in the Microsoft Windows SDK documentation) that defines elements of the data transfer.

</td>
</tr>
<tr>
<td>
IT_MSG_DEVICE_STATUS

</td>
<td>
Callback contains only status information about the device.

</td>
</tr>
<tr>
<td>
IT_MSG_FILE_PREVIEW_DATA

</td>
<td>
Indicates preview data is being transferred to the application.

</td>
</tr>
<tr>
<td>
IT_MSG_FILE_PREVIEW_DATA_HEADER

</td>
<td>
Indicates a header is being transferred to the application, prior to the preview data being transferred.

</td>
</tr>
<tr>
<td>
IT_MSG_NEW_PAGE

</td>
<td>
Indicates that the data transfer of a page is complete, and a new page is being sent.

</td>
</tr>
<tr>
<td>
IT_MSG_STATUS

</td>
<td>
Callback contains only status information about the transfer.

</td>
</tr>
<tr>
<td>
IT_MSG_TERMINATION

</td>
<td>
Indicates that the data transfer is complete.

</td>
</tr>
</table>
 


### -param lStatus [in]

Specifies the status of the transfer. This parameter is a bitwise OR of the following values:

<table>
<tr>
<th>Status</th>
<th>Definition</th>
</tr>
<tr>
<td>
IT_STATUS_TRANSFER_FROM_DEVICE

</td>
<td>
Transferring data from device.

</td>
</tr>
<tr>
<td>
IT_STATUS_PROCESSING_DATA

</td>
<td>
Device and/or minidriver are processing the data.

</td>
</tr>
<tr>
<td>
IT_STATUS_TRANSFER_TO_CLIENT

</td>
<td>
Transferring data from the minidriver to the WIA service.

</td>
</tr>
</table>
 


### -param lPercentComplete [in]

Specifies the current percentage of data transferred.


### -param lOffset [in]

Specifies the current offset (in bytes) into the transfer buffer from the beginning of the buffer.


### -param lLength [in]

Specifies the number of bytes contained in the transfer.


### -param pTranCtx [in]

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a> structure containing the data transfer values.


### -param lReserved [in]

Reserved. Set to zero.


## -returns



If the method succeeds, it returns S_OK. If the callback is canceled by the client application, the method returns S_FALSE. If the method fails, it returns a standard COM error code.




## -remarks



The percent complete values are sent directly from the driver. The WIA service does not adjust the values.

IT_MSG_FILE_PREVIEW_DATA_HEADER  is for out-of-band-data. This allows the application doing a file transfer to display the banded data. This is useful for scroll-fed scanners that have an unknown length and no preview scan. The information reported in this message should be treated the same as IT_MSG_DATA_HEADER. If a driver supports this message, it can supply preview data during its file transfer. 




## -see-also




<a href="https://msdn.microsoft.com/cf2460c5-325f-43c3-a1fe-5b6982234194">IWiaMiniDrvCallBack</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff545250">MINIDRV_TRANSFER_CONTEXT</a>
 

 

