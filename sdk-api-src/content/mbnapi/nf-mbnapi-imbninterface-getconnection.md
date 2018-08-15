---
UID: NF:mbnapi.IMbnInterface.GetConnection
title: IMbnInterface::GetConnection
author: windows-sdk-content
description: Gets the IMbnConnection object.
old-location: mbn\imbninterface_getconnection.htm
old-project: mbn
ms.assetid: 919772f5-1e86-424c-b3de-079a03bbc8e5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetConnection, GetConnection method [Microsoft Broadband Networks], GetConnection method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetConnection method, IMbnInterface.GetConnection, IMbnInterface::GetConnection, mbn.imbninterface_getconnection, mbnapi/IMbnInterface::GetConnection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnInterface.GetConnection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnInterface::GetConnection


## -description


Gets the <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> object associated with this interface.


## -parameters




### -param mbnConnection [out]

The <a href="https://msdn.microsoft.com/dae6ce6f-2534-4799-8ed3-53cd1f2eca13">IMbnConnection</a> object.


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
The method completed successfully.  <i>mbnConnection</i> contains a valid object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
Either there is no available connection or the device is not registered to a network.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 

