---
UID: NF:wmsdkidl.IWMReaderAdvanced4.SendLogParams
title: IWMReaderAdvanced4::SendLogParams
author: windows-sdk-content
description: The SendLogParams method sends log entries to the originating server. Call this method after calling AddLogParam.
old-location: wmformat\iwmreaderadvanced4_sendlogparams.htm
old-project: wmformat
ms.assetid: 3b345573-bdca-4a1f-b272-716e2ca4c88c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMReaderAdvanced4 interface [windows Media Format],SendLogParams method, IWMReaderAdvanced4.SendLogParams, IWMReaderAdvanced4::SendLogParams, IWMReaderAdvanced4SendLogParams, SendLogParams, SendLogParams method [windows Media Format], SendLogParams method [windows Media Format],IWMReaderAdvanced4 interface, wmformat.iwmreaderadvanced4_sendlogparams, wmsdkidl/IWMReaderAdvanced4::SendLogParams
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
 - IWMReaderAdvanced4.SendLogParams
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced4::SendLogParams


## -description



The <b>SendLogParams</b> method sends log entries to the originating server. Call this method after calling <b>AddLogParam</b>.




## -parameters






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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The reader is not streaming content from a remote server.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>



<a href="https://msdn.microsoft.com/7d117895-b61f-4890-8cb6-3e4ecf49ca99">IWMReaderAdvanced4::AddLogParam</a>
 

 

