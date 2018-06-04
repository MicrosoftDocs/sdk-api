---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWiaDataTransfer::idtGetData


## -description


The <b>IWiaDataTransfer::idtGetData</b> method retrieves complete files from a Windows Image Acquisition (WIA) device.


## -parameters




### -param pMedium [in, out]

Type: <b>LPSTGMEDIUM</b>

Pointer to the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure.


### -param pIWiaDataCallback [in]

Type: <b><a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a>*</b>

Pointer to the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> interface. 


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



In most respects, this method operates identically to the <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> method. The primary difference is that <b>IWiaDataTransfer::idtGetData</b> provides an additional parameter for a pointer to the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> interface. Applications use this optional parameter to obtain status notifications during the data transfer. If no status notifications are needed, it should be set to zero.

The format of the data transfer is determined by the values of the item's <a href="https://msdn.microsoft.com/library/windows/hardware/ff551553">WIA_IPA_FORMAT</a> and <b>WIA_IPA_TYMED</b> properties. The application sets these properties with calls to the <a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IWiaPropertyStorage::WriteMultiple</a> method.

Unlike the <a href="https://msdn.microsoft.com/3cbef4c0-cf28-4fdd-b347-84428ffd671b">IWiaDataTransfer::idtGetBandedData</a> method, <b>IWiaDataTransfer::idtGetData</b> transfers a complete file from a WIA device to an application rather than just a single band of data. The <i>pMedium</i> parameter is a pointer to the <a href="https://msdn.microsoft.com/5d05819a-10db-4d8e-91e4-8a7c05885cde">STGMEDIUM</a> structure which contains information on the storage medium to be used for the data transfer. Programs use the <i>pIWiaDataCallback</i> parameter to pass this method a pointer to the <a href="https://msdn.microsoft.com/c2414d68-604f-4ae7-8808-7931240b1d26">IWiaDataCallback</a> interface. Periodically, this method will use the interface pointer to invoke the <a href="https://msdn.microsoft.com/3f7fc88e-187e-41b1-a958-1f06ed81cb8f">BandedDataCallback</a> method and provide the application with status information about the data transfer in progress.

Pass <b>NULL</b> as the value of the <b>lpszFileName</b> member of the <i>pMedium</i> structure to allow WIA to determine the file name and location for the new file. Upon return, the <b>lpszFileName</b> member of the <i>pMedium</i> structure contains the location and name of the new file.

If the value returned by this method is a COM SUCCESS value or the transfer is a multipage file transfer, and the error code returned is WIA_ERROR_PAPER_JAM, WIA_ERROR_PAPER_EMPTY, or WIA_ERROR_PAPER_PROBLEM, WIA does not delete the file.



