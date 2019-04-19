---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetManualStreamSelection
title: IWMReaderAdvanced::GetManualStreamSelection (wmsdkidl.h)
author: windows-sdk-content
description: The GetManualStreamSelection method ascertains whether manual stream selection has been specified.
old-location: wmformat\iwmreaderadvanced_getmanualstreamselection.htm
tech.root: wmformat
ms.assetid: 3205f508-a24b-4d24-a5e6-be16885e941b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetManualStreamSelection, GetManualStreamSelection method [windows Media Format], GetManualStreamSelection method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetManualStreamSelection method, IWMReaderAdvanced.GetManualStreamSelection, IWMReaderAdvanced::GetManualStreamSelection, IWMReaderAdvancedGetManualStreamSelection, wmformat.iwmreaderadvanced_getmanualstreamselection, wmsdkidl/IWMReaderAdvanced::GetManualStreamSelection
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
 - IWMReaderAdvanced.GetManualStreamSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::GetManualStreamSelection


## -description



The <b>GetManualStreamSelection</b> method ascertains whether manual stream selection has been specified.




## -parameters




### -param pfSelection [out]

Pointer to a Boolean value that is True if manual selection has been specified.


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
The <i>pfSelection</i> parameter is <b>NULL</b>.

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



<a href="https://msdn.microsoft.com/en-us/library/Dd743485(v=VS.85).aspx">IWMReaderAdvanced::SetManualStreamSelection</a>
 

 

