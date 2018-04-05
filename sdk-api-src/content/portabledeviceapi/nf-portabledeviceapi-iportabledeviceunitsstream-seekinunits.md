---
UID: NF:portabledeviceapi.IPortableDeviceUnitsStream.SeekInUnits
title: IPortableDeviceUnitsStream::SeekInUnits method
author: windows-driver-content
description: The SeekInUnits method performs a seek on a stream, based on alternate units.
old-location: wpdsdk\iportabledeviceunitsstream_seekinunits.htm
old-project: wpd_sdk
ms.assetid: F94D30C7-57A8-4CBB-B416-ABB8BEC26A6E
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceUnitsStream, IPortableDeviceUnitsStream interface [Windows Portable Devices SDK], SeekInUnits method, IPortableDeviceUnitsStream::SeekInUnits, SeekInUnits method [Windows Portable Devices SDK], SeekInUnits method [Windows Portable Devices SDK], IPortableDeviceUnitsStream interface, SeekInUnits,IPortableDeviceUnitsStream.SeekInUnits, portabledeviceapi/IPortableDeviceUnitsStream::SeekInUnits, wpdsdk.iportabledeviceunitsstream_seekinunits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceUnitsStream.SeekInUnits
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceUnitsStream::SeekInUnits method


## -description


The <b>SeekInUnits</b> method performs a seek on a stream, based on alternate units.


## -parameters




### -param dlibMove [in]

The displacement to add to the location indicated by the <i>dwOrigin</i> parameter. The units for the displacement are specified by <i>units</i>. If <i>dwOrigin</i> is <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">STREAM_SEEK_SET</a>, this is interpreted as an unsigned value rather than a signed value.


### -param units [in]

The units of the <i>dlibMove</i> and <i>plibNewPosition</i> parameters.  See <a href="https://msdn.microsoft.com/BE668696-7AF3-44AA-891A-9BFF67FB5544">WPD_STREAM_UNITS</a> for more details.


### -param dwOrigin [in]

The origin for the displacement specified in <i>dlibMove</i>. The origin can be the beginning of the file (STREAM_SEEK_SET), the current seek pointer (STREAM_SEEK_CUR), or the end of the file (STREAM_SEEK_END). For more information about values, see the <a href="https://msdn.microsoft.com/ea087c6d-8854-4a81-b37b-15ab76630973">STREAM_SEEK</a> enumeration.


### -param plibNewPosition [out, optional]

A pointer to the location where this method writes the value of the new seek pointer from the beginning of the stream. The units are given by units.
You can set this pointer to NULL. In this case, this method does not provide the new seek pointer.



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
  The seek pointer was successfully adjusted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDPOINTER</b></dt>
</dl>
</td>
<td width="60%">
 Indicates that the [out] parameter <i>plibNewPosition</i> points to invalid memory, because <i>plibNewPosition</i> is not read.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INVALIDFUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwUnits</i> or <i>dwOrigin</i> parameter contains an invalid value, or the <i>dlibMove</i> parameter contains a bad offset value. For example, the result of the seek pointer is a negative offset value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4E9B2ECC-91D0-4D4F-980D-54AC88F3175D">IPortableDeviceUnitsStream</a>



<a href="https://msdn.microsoft.com/BE668696-7AF3-44AA-891A-9BFF67FB5544">WPD_STREAM_UNITS</a>
 

 

