---
UID: NF:mfidl.IMFSensorDevice.GetStreamAttributesCount
title: IMFSensorDevice::GetStreamAttributesCount
author: windows-sdk-content
description: Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.
old-location: mf\imfsensordevice_getstreamattributescount.htm
old-project: medfound
ms.assetid: C6A0C4E6-7939-42C1-A499-7C92D83CB418
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStreamAttributesCount, GetStreamAttributesCount method [Media Foundation], GetStreamAttributesCount method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetStreamAttributesCount method, IMFSensorDevice.GetStreamAttributesCount, IMFSensorDevice::GetStreamAttributesCount, mf.imfsensordevice_getstreamattributescount, mfidl/IMFSensorDevice::GetStreamAttributesCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfplat.lib
-	mfplat.dll
-	mfplat.dll
-	mfplat.dll.dll
api_name:
-	IMFSensorDevice.GetStreamAttributesCount
product: Windows
targetos: Windows
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSensorDevice::GetStreamAttributesCount


## -description


Gets the count of stream attribute stores for the sensor device. This number represents the number of total streams available for the device because every valid stream must have an attribute store that contains at least the stream ID and stream category.


## -parameters




### -param eType [in]

A member of the <a href="https://msdn.microsoft.com/598AE9EC-3B8D-419A-A6A9-02DCDD459162">MFSensorStreamType</a> enumeration specifying whether the attribute store count is being requested for an input or output stream.  


### -param pdwCount [out]

The number of stream attributes available for this sensor device. 


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">

                The <i>pdwCount</i> parameter is null.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">

                The sensor group has not been initialized.

</td>
</tr>
</table>
 




## -remarks



The caller can use the number of stream attributes to indicate the number of streams provided by the sensor device.  

<div class="alert"><b>Note</b>  Depending on the sharing mode in which the sensor device was activated, not all streams may be present during runtime.  Streams marked as shared, i.e. with the <a href="https://msdn.microsoft.com/15DF88A2-041C-4E73-A121-00454964E2C1">MF_DEVICESTREAM_FRAMESERVER_SHARED</a> attribute set to non-zero value, and streams with pins with the category <b>PINNAME_VIDEO_PREVIEW</b> will be present in devices that are set to used shared mode. Put a device in shared mode by passing <a href="https://msdn.microsoft.com/D405AB48-13EC-4859-91B6-0DB797F85DBE">MFSensorDeviceMode_Shared</a> into <a href="https://msdn.microsoft.com/2B0DC098-EA3B-4061-8191-C67BA54663A3">SetSensorDeviceMode</a>.
If no streams are marked as shared and no preview stream is available, the first capture stream, with the category <b>PINNAME_VIDEO_CAPTURE</b>,  will be shared.
</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

