---
UID: NF:wmsdkidl.IWMProfile.GetStreamCount
title: IWMProfile::GetStreamCount
author: windows-sdk-content
description: The GetStreamCount method retrieves the number of streams in a profile.
old-location: wmformat\iwmprofile_getstreamcount.htm
tech.root: wmformat
ms.assetid: 49534bc3-9115-422b-b448-b6f9c6ec1c47
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetStreamCount, GetStreamCount method [windows Media Format], GetStreamCount method [windows Media Format],IWMProfile interface, GetStreamCount method [windows Media Format],IWMProfile2 interface, GetStreamCount method [windows Media Format],IWMProfile3 interface, IWMProfile interface [windows Media Format],GetStreamCount method, IWMProfile.GetStreamCount, IWMProfile2 interface [windows Media Format],GetStreamCount method, IWMProfile2::GetStreamCount, IWMProfile3 interface [windows Media Format],GetStreamCount method, IWMProfile3::GetStreamCount, IWMProfile::GetStreamCount, IWMProfileGetStreamCount, wmformat.iwmprofile_getstreamcount, wmsdkidl/IWMProfile2::GetStreamCount, wmsdkidl/IWMProfile3::GetStreamCount, wmsdkidl/IWMProfile::GetStreamCount
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
 - qasf.dll
api_name:
 - IWMProfile.GetStreamCount
 - IWMProfile2.GetStreamCount
 - IWMProfile3.GetStreamCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile::GetStreamCount


## -description



The <b>GetStreamCount</b> method retrieves the number of streams in a profile.




## -parameters




### -param pcStreams [out]

Pointer to a count of streams.


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
The <i>pcStreams</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>
 

 

