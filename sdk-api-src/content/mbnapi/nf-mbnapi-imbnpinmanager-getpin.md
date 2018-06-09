---
UID: NF:mbnapi.IMbnPinManager.GetPin
title: IMbnPinManager::GetPin
author: windows-sdk-content
description: Gets a specific type of PIN.
old-location: mbn\imbnpinmanager_getpin.htm
old-project: mbn
ms.assetid: 21752fb9-db6b-4fd1-9c6f-a756408bda53
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetPin, GetPin method [Microsoft Broadband Networks], GetPin method [Microsoft Broadband Networks],IMbnPinManager interface, IMbnPinManager interface [Microsoft Broadband Networks],GetPin method, IMbnPinManager.GetPin, IMbnPinManager::GetPin, mbn.imbnpinmanager_getpin, mbnapi/IMbnPinManager::GetPin
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MBN_VOICE_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnPinManager.GetPin
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnPinManager::GetPin


## -description


Gets a specific type of PIN.


## -parameters




### -param pinType [in]

An <a href="https://msdn.microsoft.com/79791522-cf6b-4dae-a9c2-68e9e2fc394f">MBN_PIN_TYPE</a> value that represents the requested PIN type.


### -param pin [out, retval]

Pointer to the address of the <a href="https://msdn.microsoft.com/76764dbb-7de0-4b95-a210-60b8e6a4b24b">IMbnPin</a> for the requested PIN type.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Otherwise, the calling application must release this interface when it is done using it.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The PIN type is not available.  The Mobile Broadband service is currently probing the device to retrieve this information.  When the PIN type is available, the Mobile Broadband service will call the <a href="https://msdn.microsoft.com/37347dd8-07c2-4521-a5f0-a51053634704">OnPinListAvailable</a> method of <a href="https://msdn.microsoft.com/2942bd4d-5bdb-45eb-a008-352bf44eec80">IMbnPinManagerEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A PIN is required for the operation to complete.  The calling Application can retry this operation when device is PIN unlocked

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
There is no SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
There is a bad SIM in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The requested PIN type is not supported by the device.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b5cfabc7-81f8-4ea0-b6f4-5de011320f0b">IMbnPinManager</a>
 

 

