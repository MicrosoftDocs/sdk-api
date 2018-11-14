---
UID: NF:mfidl.IMFSystemId.GetData
title: IMFSystemId::GetData
author: windows-sdk-content
description: Retrieves system id data.
old-location: mf\imfsystemid_getdata.htm
tech.root: medfound
ms.assetid: 5b345a8d-65d1-4780-a7b9-b1025f9fa773
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetData, GetData method [Media Foundation], GetData method [Media Foundation],IMFSystemId interface, IMFSystemId interface [Media Foundation],GetData method, IMFSystemId.GetData, IMFSystemId::GetData, mf.imfsystemid_getdata, mfidl/IMFSystemId::GetData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFSystemId.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfidl.h
: 
- IMFSystemId.GetData
: 
---

# IMFSystemId::GetData


## -description


Retrieves system id data.


## -parameters




### -param size

The size in bytes of the returned data.


### -param data

Receives the returned data.  The caller must free this buffer by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


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
 




## -see-also




<a href="https://msdn.microsoft.com/45c80fc5-5ea7-4d4e-9c9c-5a38f62b2d28">IMFSystemId</a>
 

 

