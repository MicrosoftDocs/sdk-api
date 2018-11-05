---
UID: NF:strmif.IPin.QueryAccept
title: IPin::QueryAccept
author: windows-sdk-content
description: The QueryAccept method determines whether the pin accepts a specified media type.
old-location: dshow\ipin_queryaccept.htm
tech.root: DirectShow
ms.assetid: ed11eeef-464b-4a75-958b-2bc6dbc7af04
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IPin interface [DirectShow],QueryAccept method, IPin.QueryAccept, IPin::QueryAccept, IPinQueryAccept, QueryAccept, QueryAccept method [DirectShow], QueryAccept method [DirectShow],IPin interface, dshow.ipin_queryaccept, strmif/IPin::QueryAccept
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPin.QueryAccept
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::QueryAccept


## -description



The <code>QueryAccept</code> method determines whether the pin accepts a specified media type.




## -parameters




### -param pmt [in]

Pointer to an <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the media type.


## -returns



Returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The pin rejects the media type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The pin accepts the media type.

</td>
</tr>
</table>
 




## -remarks



A return value of S_OK indicates that the pin will accept the media type, either on the next sample, or after a pin reconnection. The implementation should take into account the current state of the filter, including connections on other pins, and any properties that can be set on the filter.

Any other return value, including S_FALSE, means that the pin rejects the media type. Therefore, test for S_OK explicitly; do not use the <b>SUCCEEDED</b> macro.

If the filter is running, a return value of S_OK is ambiguous. The pin might accept a format change on the next media sample, without reconnecting; or it might need to reconnect. If the pin supports the <a href="https://msdn.microsoft.com/0843a01c-6f6a-4765-abca-dd562175fcee">IPinConnection</a> interface, call the <a href="https://msdn.microsoft.com/86a4f18c-4bd0-45d2-bb5a-b0f41cd0ab43">IPinConnection::DynamicQueryAccept</a> method, which specifically tests whether the pin can accept the new type without reconnecting.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/ff60de5a-3edc-405d-aa02-8704b96d5e87">Dynamic Format Changes</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

