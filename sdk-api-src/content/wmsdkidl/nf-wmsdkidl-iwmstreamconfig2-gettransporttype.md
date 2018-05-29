---
UID: NF:wmsdkidl.IWMStreamConfig2.GetTransportType
title: IWMStreamConfig2::GetTransportType
author: windows-sdk-content
description: The GetTransportType method retrieves the type of data communication protocol (reliable or unreliable) used for the stream.
old-location: wmformat\iwmstreamconfig2_gettransporttype.htm
old-project: wmformat
ms.assetid: dfe7b285-8d1d-4b71-a839-1c73d76e6444
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetTransportType, GetTransportType method [windows Media Format], GetTransportType method [windows Media Format],IWMStreamConfig2 interface, IWMStreamConfig2 interface [windows Media Format],GetTransportType method, IWMStreamConfig2.GetTransportType, IWMStreamConfig2::GetTransportType, IWMStreamConfig2GetTransportType, wmformat.iwmstreamconfig2_gettransporttype, wmsdkidl/IWMStreamConfig2::GetTransportType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
api_name:
-	IWMStreamConfig2.GetTransportType
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamConfig2::GetTransportType


## -description



The <b>GetTransportType</b> method retrieves the type of data communication protocol (reliable or unreliable) used for the stream.




## -parameters




### -param pnTransportType [out]

Pointer to a variable that receives one member of the <a href="https://msdn.microsoft.com/1d689487-f71b-4b27-928c-c55bd22579ed">WMT_TRANSPORT_TYPE</a> enumeration type.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pnTransportType</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/89958c80-2140-49ab-b696-189e8f722e96">IWMStreamConfig2::SetTransportType</a>
 

 

