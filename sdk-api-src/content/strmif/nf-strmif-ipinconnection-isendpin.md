---
UID: NF:strmif.IPinConnection.IsEndPin
title: IPinConnection::IsEndPin (strmif.h)
author: windows-sdk-content
description: The IsEndPin method indicates whether a reconnection search should end at this pin.
old-location: dshow\ipinconnection_isendpin.htm
tech.root: DirectShow
ms.assetid: e078c952-2c3b-48cd-a898-ac2de9fc359a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPinConnection interface [DirectShow],IsEndPin method, IPinConnection.IsEndPin, IPinConnection::IsEndPin, IPinConnectionIsEndPin, IsEndPin, IsEndPin method [DirectShow], IsEndPin method [DirectShow],IPinConnection interface, dshow.ipinconnection_isendpin, strmif/IPinConnection::IsEndPin
ms.topic: method
f1_keywords: 
 - "strmif/IPinConnection.IsEndPin"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IPinConnection.IsEndPin
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPinConnection::IsEndPin


## -description



The <code>IsEndPin</code> method indicates whether a reconnection search should end at this pin.




## -parameters






## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
This pin is not a candidate for reconnection. (The reconnection search should not stop at this pin.)

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
This pin is a candidate for reconnection. (The reconnection search should stop at this pin.)

</td>
</tr>
</table>
 




## -remarks



A filter or application can call this method to determine whether the pin is a candidate for dynamic reconnection.

Generally, a sink filter or a filter that splits or merges data should return S_OK. Other filters (for example, simple transform filters) should return S_FALSE.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dynamic-reconnection">Dynamic Reconnection</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipinconnection">IPinConnection Interface</a>
 

 

