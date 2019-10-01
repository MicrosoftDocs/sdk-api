---
UID: NF:mfidl.IMFSystemId.GetData
title: IMFSystemId::GetData (mfidl.h)
author: windows-sdk-content
description: Retrieves system id data.
old-location: mf\imfsystemid_getdata.htm
tech.root: medfound
ms.assetid: 5b345a8d-65d1-4780-a7b9-b1025f9fa773
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Media Foundation], GetData method [Media Foundation],IMFSystemId interface, IMFSystemId interface [Media Foundation],GetData method, IMFSystemId.GetData, IMFSystemId::GetData, mf.imfsystemid_getdata, mfidl/IMFSystemId::GetData
ms.topic: method
f1_keywords: 
 - "mfidl/IMFSystemId.GetData"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSystemId::GetData


## -description


Retrieves system id data.


## -parameters




### -param size

The size in bytes of the returned data.


### -param data

Receives the returned data.  The caller must free this buffer by calling <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfsystemid">IMFSystemId</a>
 

 

