---
UID: NF:wmsdkidl.IWMPacketSize.GetMaxPacketSize
title: IWMPacketSize::GetMaxPacketSize method
author: windows-driver-content
description: The GetMaxPacketSize method retrieves the maximum size of a packet in an ASF file.
old-location: wmformat\iwmpacketsize_getmaxpacketsize.htm
old-project: wmformat
ms.assetid: 8410c524-9c27-48ac-9a48-c17cae782764
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: GetMaxPacketSize method [windows Media Format], GetMaxPacketSize method [windows Media Format], IWMPacketSize interface, GetMaxPacketSize method [windows Media Format], IWMPacketSize2 interface, GetMaxPacketSize,IWMPacketSize.GetMaxPacketSize, IWMPacketSize, IWMPacketSize interface [windows Media Format], GetMaxPacketSize method, IWMPacketSize2 interface [windows Media Format], GetMaxPacketSize method, IWMPacketSize2::GetMaxPacketSize, IWMPacketSize::GetMaxPacketSize, IWMPacketSizeGetMaxPacketSize, wmformat.iwmpacketsize_getmaxpacketsize, wmsdkidl/IWMPacketSize2::GetMaxPacketSize, wmsdkidl/IWMPacketSize::GetMaxPacketSize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
-	qasf.dll
api_name:
-	IWMPacketSize.GetMaxPacketSize
-	IWMPacketSize2.GetMaxPacketSize
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPacketSize::GetMaxPacketSize method


## -description



The <b>GetMaxPacketSize</b> method retrieves the maximum size of a <a href="wmformat_glossary.htm">packet</a> in an ASF file. 




## -parameters




### -param pdwMaxPacketSize [out]

Pointer to a <b>DWORD</b> containing the maximum packet size, in bytes.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwMaxPacketSize</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information, see the Remarks section of <a href="https://msdn.microsoft.com/a8230c08-e60f-454d-93a5-037685d6151c">SetMaxPacketSize</a>.




## -see-also




<a href="https://msdn.microsoft.com/002442fe-46de-49d9-8aff-ad7c9aabc8d1">IWMPacketSize Interface</a>



<a href="https://msdn.microsoft.com/4af4c088-9fc3-46a9-8451-518b11bc94e3">IWMPacketSize2</a>
 

 

