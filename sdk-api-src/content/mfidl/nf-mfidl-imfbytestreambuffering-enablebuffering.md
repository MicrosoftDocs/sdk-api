---
UID: NF:mfidl.IMFByteStreamBuffering.EnableBuffering
title: IMFByteStreamBuffering::EnableBuffering
author: windows-sdk-content
description: Enables or disables buffering.
old-location: mf\imfbytestreambuffering_enablebuffering.htm
old-project: medfound
ms.assetid: 5f7418ff-32e5-49b3-b7b3-6686e6562d51
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 5f7418ff-32e5-49b3-b7b3-6686e6562d51, EnableBuffering, EnableBuffering method [Media Foundation], EnableBuffering method [Media Foundation],IMFByteStreamBuffering interface, IMFByteStreamBuffering interface [Media Foundation],EnableBuffering method, IMFByteStreamBuffering.EnableBuffering, IMFByteStreamBuffering::EnableBuffering, mf.imfbytestreambuffering_enablebuffering, mfidl/IMFByteStreamBuffering::EnableBuffering
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStreamBuffering.EnableBuffering
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStreamBuffering::EnableBuffering


## -description



Enables or disables buffering.




## -parameters




### -param fEnable [in]

Specifies whether the byte stream buffers data. If <b>TRUE</b>, buffering is enabled. If <b>FALSE</b>, buffering is disabled.


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
</table>
 




## -remarks



Before calling this method, call <a href="https://msdn.microsoft.com/033ea7d4-d669-497b-be37-a8c9a6584209">IMFByteStreamBuffering::SetBufferingParams</a> to set the buffering parameters on the byte stream.




## -see-also




<a href="https://msdn.microsoft.com/bbf9cdb1-5ec7-498a-aa59-85c24779547e">IMFByteStreamBuffering</a>
 

 

