---
UID: NF:wmsdkidl.IWMReaderAdvanced2.GetLogClientID
title: IWMReaderAdvanced2::GetLogClientID
author: windows-sdk-content
description: The GetLogClientID method queries whether the reader logs the client's unique ID or an anonymous session ID.
old-location: wmformat\iwmreaderadvanced2_getlogclientid.htm
tech.root: wmformat
ms.assetid: 034ad344-2266-4662-9797-70031f58f0cd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetLogClientID, GetLogClientID method [windows Media Format], GetLogClientID method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced2 interface [windows Media Format],GetLogClientID method, IWMReaderAdvanced2.GetLogClientID, IWMReaderAdvanced2::GetLogClientID, IWMReaderAdvanced2GetLogClientID, wmformat.iwmreaderadvanced2_getlogclientid, wmsdkidl/IWMReaderAdvanced2::GetLogClientID
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMReaderAdvanced2.GetLogClientID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmsdkidl.h
: 
- IWMReaderAdvanced2.GetLogClientID
: 
---

# IWMReaderAdvanced2::GetLogClientID


## -description



The <b>GetLogClientID</b> method queries whether the reader logs the client's unique ID or an anonymous session ID.




## -parameters




### -param pfLogClientID [out]

Pointer Boolean value that is set to True if the client's log ID must be sent to the server.


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
A <b>NULL</b> or invalid argument was passed in.

</td>
</tr>
</table>
 




## -remarks



See the remarks for <b>SetLogClientID</b>.




## -see-also




<a href="https://msdn.microsoft.com/3e0d0fea-4370-41f8-b461-73a37de8d8bc">Client Logging</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/818b7a0e-bbf4-42b2-a5a4-75078834c9f6">IWMReaderAdvanced2::SetLogClientID</a>
 

 

