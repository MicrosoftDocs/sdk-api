---
UID: NF:wia_xp.IWiaDataTransfer.idtGetBandedData
title: IWiaDataTransfer::idtGetBandedData
author: windows-sdk-content
description: The IWiaDataTransfer::idtGetBandedData method transfers a band of data from a hardware device to an application. For efficiency, applications retrieve data from Windows Image Acquisition (WIA) hardware devices in successive bands.
old-location: wia\_wia_IWiaDataTransfer_idtGetBandedData.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiadatatransfer\idtgetbandeddata.htm
ms.author: windowssdkdev
ms.date: 05/03/2018
ms.keywords: IWiaDataTransfer interface [WIA],idtGetBandedData method, IWiaDataTransfer.idtGetBandedData, IWiaDataTransfer::idtGetBandedData, _wia_IWiaDataTransfer_idtGetBandedData, idtGetBandedData, idtGetBandedData method [WIA], idtGetBandedData method [WIA],IWiaDataTransfer interface, wia._wia_IWiaDataTransfer_idtGetBandedData, wia_xp/IWiaDataTransfer::idtGetBandedData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaservc.dll
api_name:
-	IWiaDataTransfer.idtGetBandedData
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWiaDataTransfer::idtGetBandedData


## -description


The <b>IWiaDataTransfer::idtGetBandedData</b> method transfers a band of data from a hardware device to an application. For efficiency, applications retrieve data from Windows Image Acquisition (WIA) hardware devices in successive bands. 


## -parameters




### -param pWiaDataTransInfo [in]

Type: <b>PWIA_DATA_TRANSFER_INFO</b>

Pointer to the <a href="https://msdn.microsoft.com/4b20e695-d414-4bf9-821e-2402e37efdd1">WIA_DATA_TRANSFER_INFO</a> structure.


### -param pIWiaDataCallback [in]

Type: <b><a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> interface. Periodically, this method will call the <a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">BandedDataCallback</a> method to provide the application with data transfer status notification.


## -returns



Type: <b>HRESULT</b>

This method can return any one of the following values:

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>One or more parameters to this method contain invalid data.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>This method cannot allocate enough memory to complete its operation.</td>
</tr>
<tr>
<td>E_UNEXPECTED</td>
<td>An unknown error occurred.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>The application canceled the operation.</td>
</tr>
<tr>
<td>S_OK</td>
<td>The image was successfully acquired.</td>
</tr>
<tr>
<td>STG_E_MEDIUMFULL</td>
<td>The storage medium the application is using to acquire the image is full.</td>
</tr>
<tr>
<td>WIA_S_NO_DEVICE_AVAILABLE</td>
<td>There are no WIA hardware devices attached to the user's computer.</td>
</tr>
</table>
 

This method will return a value specified in <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>, or a standard COM error if it fails for any reason other than those specified in the preceding table.




## -remarks



The <b>IWiaDataTransfer::idtGetBandedData</b> method allocates a section of memory to transfer data without requiring an extra data copy through the Component Object Model/Remote Procedure Call (COM/RPC) marshalling layer. This memory section is shared between the application and the hardware device's item tree.

Optionally, the application can pass in a pointer to a block of memory that <b>IWiaDataTransfer::idtGetBandedData</b> will use as its shared section. The application passes this handle by storing the pointer in the <b>ulSection</b> member of the <a href="https://msdn.microsoft.com/4b20e695-d414-4bf9-821e-2402e37efdd1">WIA_DATA_TRANSFER_INFO</a> structure prior to calling <b>IWiaDataTransfer::idtGetBandedData</b>.

Applications can improve performance by using double buffering. To do this, applications must set the <b>bDoubleBuffer</b> member of the <a href="https://msdn.microsoft.com/4b20e695-d414-4bf9-821e-2402e37efdd1">WIA_DATA_TRANSFER_INFO</a> structure to <b>TRUE</b>. The <b>IWiaDataTransfer::idtGetBandedData</b> method will divide the data buffer in half. When one half of the buffer is full, <b>IWiaDataTransfer::idtGetBandedData</b> will send a notification to the application using the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> pointer passed in through the <i>pIWiaDataCallback</i> parameter. While the application is retrieving the data from the full half of the buffer, the device driver can fill the other half with data.

The format of the data transfer is determined by the values of the item's <a href="https://msdn.microsoft.com/library/windows/hardware/ff551553">WIA_IPA_FORMAT</a> and <b>WIA_IPA_TYMED</b> properties. The application sets these properties with calls to the <a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IWiaPropertyStorage::WriteMultiple</a> method.



