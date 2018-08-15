---
UID: NF:wmsdkidl.IWMWriterAdvanced.IsRealTime
title: IWMWriterAdvanced::IsRealTime
author: windows-sdk-content
description: The IsRealTime method ascertains whether the writer is running in real time.
old-location: wmformat\iwmwriteradvanced_isrealtime.htm
old-project: wmformat
ms.assetid: 3d00eb78-d90e-41a0-9bba-305ac65057f3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMWriterAdvanced interface [windows Media Format],IsRealTime method, IWMWriterAdvanced.IsRealTime, IWMWriterAdvanced::IsRealTime, IWMWriterAdvancedIsRealTime, IsRealTime, IsRealTime method [windows Media Format], IsRealTime method [windows Media Format],IWMWriterAdvanced interface, wmformat.iwmwriteradvanced_isrealtime, wmsdkidl/IWMWriterAdvanced::IsRealTime
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterAdvanced.IsRealTime
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced::IsRealTime


## -description



The <b>IsRealTime</b> method ascertains whether the writer is running in real time.




## -parameters




### -param pfRealTime [out]

Pointer to a Boolean value that is True if the writer is running in real time.


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
<i>pfRealTime</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If the writer is running in real time, the application can get the current time from it.

By default, the writer does not run in real time.




## -see-also




<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>
 

 

