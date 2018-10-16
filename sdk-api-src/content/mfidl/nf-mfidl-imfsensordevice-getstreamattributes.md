---
UID: NF:mfidl.IMFSensorDevice.GetStreamAttributes
title: IMFSensorDevice::GetStreamAttributes
author: windows-sdk-content
description: Gets the stream attribute store with the specified index.
old-location: mf\imfsensordevice_getstreamattributes.htm
tech.root: medfound
ms.assetid: DDBEB335-E6E3-4185-B7EF-90FABA9CDCE5
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetStreamAttributes, GetStreamAttributes method [Media Foundation], GetStreamAttributes method [Media Foundation],IMFSensorDevice interface, IMFSensorDevice interface [Media Foundation],GetStreamAttributes method, IMFSensorDevice.GetStreamAttributes, IMFSensorDevice::GetStreamAttributes, mf.imfsensordevice_getstreamattributes, mfidl/IMFSensorDevice::GetStreamAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Mfplat.lib; Mfplat.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplat.lib
 - mfplat.dll
 - mfplat.dll
 - mfplat.dll.dll
api_name:
 - IMFSensorDevice.GetStreamAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSensorDevice::GetStreamAttributes


## -description


Gets the stream attribute store with the specified index.


## -parameters




### -param eType [in]

A member of the <a href="https://msdn.microsoft.com/598AE9EC-3B8D-419A-A6A9-02DCDD459162">MFSensorStreamType</a> enumeration specifying whether the attribute store is being requested for an input or output stream.  


### -param dwIndex [in]

The 0-based index of the stream to be retrieved.  The index must be between 0 and the value returned by <a href="https://msdn.microsoft.com/C6A0C4E6-7939-42C1-A499-7C92D83CB418">GetStreamAttributesCount</a> - 1.


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface representing a copy internal attribute store of the stream.


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
The <i>pDeviceId</i> parameter is null.

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



The object returned is a copy of the internal attribute store and so changes made to the returned attributes have no effect on the <a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/061EF002-178E-42CA-9D32-7E1282297BA4">IMFSensorDevice</a>
 

 

