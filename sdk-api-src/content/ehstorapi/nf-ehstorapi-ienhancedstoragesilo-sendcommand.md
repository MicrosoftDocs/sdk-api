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

# IEnhancedStorageSilo::SendCommand


## -description


Sends a raw silo command to the silo object. This method is utilized to communicate with a silo which is not represented by a driver. 


## -parameters




### -param Command




### -param pbCommandBuffer [in]

The command payload sent to the device in the send data phase of the command.


### -param cbCommandBuffer [in]

The count of bytes contained in the <i>pbCommandBuffer</i> buffer.


### -param pbResponseBuffer [out]

The response payload that is returned to the host from the device in the receive data phase of the command.


### -param pcbResponseBuffer [out]

On method entry, contains the size of <i>pbResponseBuffer</i> in bytes. On method exit, it contains the count of bytes contained in the returned <i>pbResponse</i> buffer.


#### - ulCommand [in]

The silo command to be issued. 8 bits of this value are placed in the byte at position 3 of the CDB sent to the device; i.e. the second byte of the <b>SecurityProtocolSpecific</b> field.


## -returns



This method can return one of these values.

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
Silo command completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pbCommandBuffer, pbResponseBuffer, or pcbResponseBuffer parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_ENOUGH_MEMORY)</b></dt>
</dl>
</td>
<td width="60%">
The size of pbResponseBuffer is insufficient to contain the response data.

</td>
</tr>
</table>
 




## -remarks



This method is currently not supported by the IEEE 1667 certificate and password silos. It is recommended that the <a href="https://msdn.microsoft.com/b848a866-9fdf-4cb3-b289-6df5fc1bf723">Enhanced Storage Portable Device Commands</a> are used instead.

The caller is responsible for sending correct parameters to the command, as well as allocating the necessary buffer for the returned results.




## -see-also




<a href="https://msdn.microsoft.com/b848a866-9fdf-4cb3-b289-6df5fc1bf723">Enhanced Storage Portable Device Commands</a>



<a href="https://msdn.microsoft.com/041e66d2-f772-407d-85f7-71f226c7ec4b">IEnhancedStorageSilo</a>
 

 

