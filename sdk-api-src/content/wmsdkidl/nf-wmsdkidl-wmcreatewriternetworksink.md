---
UID: NF:wmsdkidl.WMCreateWriterNetworkSink
title: WMCreateWriterNetworkSink function
author: windows-sdk-content
description: The WMCreateWriterNetworkSink function creates a writer network sink object.
old-location: wmformat\wmcreatewriternetworksink.htm
old-project: wmformat
ms.assetid: 5d391867-dece-4d40-80e2-99071d332984
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WMCreateWriterNetworkSink, WMCreateWriterNetworkSink function [windows Media Format], wmformat.wmcreatewriternetworksink, wmsdkidl/WMCreateWriterNetworkSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateWriterNetworkSink
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WMCreateWriterNetworkSink function


## -description



The <b>WMCreateWriterNetworkSink</b> function creates a writer network sink object.




## -parameters




### -param ppSink [out]

Pointer to a pointer to the <a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink</a> interface of the newly created writer network sink object.


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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10fa8f96-8030-4727-af5d-7c06229d05d8">Functions</a>



<a href="https://msdn.microsoft.com/f7765b42-693a-4f48-b750-17579e860b6d">Writer Network Sink Object</a>
 

 

