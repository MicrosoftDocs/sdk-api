---
UID: NF:mfidl.IMFMediaSourceEx.GetSourceAttributes
title: IMFMediaSourceEx::GetSourceAttributes
author: windows-driver-content
description: Gets an attribute store for the media source.
old-location: mf\imfmediasourceex_getsourceattributes.htm
old-project: medfound
ms.assetid: A58A2537-1ABD-4EC5-AC84-A5FFA7127CEB
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetSourceAttributes, GetSourceAttributes method [Media Foundation], GetSourceAttributes method [Media Foundation],IMFMediaSourceEx interface, IMFMediaSourceEx interface [Media Foundation],GetSourceAttributes method, IMFMediaSourceEx.GetSourceAttributes, IMFMediaSourceEx::GetSourceAttributes, mf.imfmediasourceex_getsourceattributes, mfidl/IMFMediaSourceEx::GetSourceAttributes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfidl.h
api_name:
-	IMFMediaSourceEx.GetSourceAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSourceEx::GetSourceAttributes


## -description


Gets an attribute store for the media source.


## -parameters




### -param ppAttributes [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. The caller must release the interface.


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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support source-level attributes.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer to get or set attributes that apply to the entire source. For stream-level attributes, use the <a href="https://msdn.microsoft.com/360B64E6-4936-4E40-A0EB-7E9EBAF1203E">IMFMediaSourceEx::GetStreamAttributes</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/C72C79D5-FD65-4F27-A8C8-B94BF5A9E829">IMFMediaSourceEx</a>
 

 

