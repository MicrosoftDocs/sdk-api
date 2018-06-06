---
UID: NF:wmsdkidl.IWMStreamList.AddStream
title: IWMStreamList::AddStream
author: windows-sdk-content
description: The AddStream method adds a stream to the list.
old-location: wmformat\iwmstreamlist_addstream.htm
old-project: wmformat
ms.assetid: 20aeed9d-029b-4b60-9ff3-14555bd53eb9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: AddStream, AddStream method [windows Media Format], AddStream method [windows Media Format],IWMStreamList interface, IWMStreamList interface [windows Media Format],AddStream method, IWMStreamList.AddStream, IWMStreamList::AddStream, IWMStreamListAddStream, wmformat.iwmstreamlist_addstream, wmsdkidl/IWMStreamList::AddStream
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMStreamList.AddStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMStreamList::AddStream


## -description



The <b>AddStream</b> method adds a stream to the list.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough available memory.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList Interface</a>



<a href="https://msdn.microsoft.com/3b69f516-a321-49f1-a299-666143eaf8a5">IWMStreamList::RemoveStream</a>
 

 

