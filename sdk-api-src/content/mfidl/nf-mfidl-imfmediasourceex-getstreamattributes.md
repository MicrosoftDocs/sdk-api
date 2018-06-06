---
UID: NF:mfidl.IMFMediaSourceEx.GetStreamAttributes
title: IMFMediaSourceEx::GetStreamAttributes
author: windows-sdk-content
description: Gets an attribute store for a stream on the media source.
old-location: mf\imfmediasourceex_getstreamattributes.htm
old-project: medfound
ms.assetid: 360B64E6-4936-4E40-A0EB-7E9EBAF1203E
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: GetStreamAttributes, GetStreamAttributes method [Media Foundation], GetStreamAttributes method [Media Foundation],IMFMediaSourceEx interface, IMFMediaSourceEx interface [Media Foundation],GetStreamAttributes method, IMFMediaSourceEx.GetStreamAttributes, IMFMediaSourceEx::GetStreamAttributes, mf.imfmediasourceex_getstreamattributes, mfidl/IMFMediaSourceEx::GetStreamAttributes
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFMediaSourceEx.GetStreamAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSourceEx::GetStreamAttributes


## -description


Gets an attribute store for a stream on the media source.


## -parameters




### -param dwStreamIdentifier [in]

The identifier of the stream. To get the identifier, call <a href="https://msdn.microsoft.com/d282ee48-6145-4557-8fa7-786b893327fa">IMFStreamDescriptor::GetStreamIdentifier</a> on the stream descriptor.


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
The media source does not support stream-level attributes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream identifier.

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> pointer to get or set attributes that apply to the specified stream. For attributes that apply to the entire source, use the <a href="https://msdn.microsoft.com/A58A2537-1ABD-4EC5-AC84-A5FFA7127CEB">IMFMediaSourceEx::GetSourceAttributes</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/C72C79D5-FD65-4F27-A8C8-B94BF5A9E829">IMFMediaSourceEx</a>
 

 

