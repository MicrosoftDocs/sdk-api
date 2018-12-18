---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetStreamSelected
title: IWMReaderAdvanced::GetStreamSelected
author: windows-sdk-content
description: The GetStreamSelected method ascertains whether a particular stream is currently selected. This method can be used only when manual stream selection has been specified.
old-location: wmformat\iwmreaderadvanced_getstreamselected.htm
tech.root: wmformat
ms.assetid: 083fc743-79be-43c6-ac4b-458c74f42fa0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStreamSelected, GetStreamSelected method [windows Media Format], GetStreamSelected method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetStreamSelected method, IWMReaderAdvanced.GetStreamSelected, IWMReaderAdvanced::GetStreamSelected, IWMReaderAdvancedGetStreamSelected, wmformat.iwmreaderadvanced_getstreamselected, wmsdkidl/IWMReaderAdvanced::GetStreamSelected
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
 - IWMReaderAdvanced.GetStreamSelected
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced::GetStreamSelected


## -description



The <b>GetStreamSelected</b> method ascertains whether a particular stream is currently selected. This method can be used only when manual stream selection has been specified.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


### -param pSelection [out]

Pointer to one member of the <a href="https://msdn.microsoft.com/en-us/library/Dd757857(v=VS.85).aspx">WMT_STREAM_SELECTION</a> enumeration type.


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
The <i>pSelection</i> parameter is <b>NULL</b>, or the stream number is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The reader object has not opened a file yet.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743488(v=VS.85).aspx">IWMReaderAdvanced::SetStreamsSelected</a>



<a href="https://msdn.microsoft.com/49ec283f-670a-4a0e-9477-c60a80919a1e">To Use Manual Stream Selection</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757857(v=VS.85).aspx">WMT_STREAM_SELECTION</a>
 

 

