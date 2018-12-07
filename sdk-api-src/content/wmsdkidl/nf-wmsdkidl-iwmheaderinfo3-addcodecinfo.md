---
UID: NF:wmsdkidl.IWMHeaderInfo3.AddCodecInfo
title: IWMHeaderInfo3::AddCodecInfo
author: windows-sdk-content
description: The AddCodecInfo method adds codec information to a file. When you copy a compressed stream from one file to another, use this method to include the information about the encoding codec in the file header.
old-location: wmformat\iwmheaderinfo3_addcodecinfo.htm
tech.root: wmformat
ms.assetid: 4c5bc019-e4bb-419b-91ce-779fd36d7b4c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddCodecInfo, AddCodecInfo method [windows Media Format], AddCodecInfo method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo3 interface [windows Media Format],AddCodecInfo method, IWMHeaderInfo3.AddCodecInfo, IWMHeaderInfo3::AddCodecInfo, IWMHeaderInfo3AddCodecInfo, wmformat.iwmheaderinfo3_addcodecinfo, wmsdkidl/IWMHeaderInfo3::AddCodecInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMHeaderInfo3.AddCodecInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMHeaderInfo3::AddCodecInfo


## -description



The <b>AddCodecInfo</b> method adds codec information to a file. When you copy a compressed stream from one file to another, use this method to include the information about the encoding codec in the file header.




## -parameters




### -param pwszName [in]

Pointer to a wide-character null-terminated string containing the name.


### -param pwszDescription [in]

Pointer to a wide-character null-terminated string containing the description.


### -param codecType [in]

A value from the <a href="https://msdn.microsoft.com/31fcaa84-1b7e-407c-95dc-bf13263b788a">WMT_CODEC_INFO_TYPE</a> enumeration specifying the codec type.


### -param cbCodecInfo [in]

The size of the codec information, in bytes.


### -param pbCodecInfo [in]

Pointer to an array of bytes that contains the codec information.


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
</table>
 




## -remarks



The parameters passed to this method should be obtained from the original file with a call to <a href="https://msdn.microsoft.com/685eaf9e-6cc8-4c38-be34-afa4b504a326">IWMHeaderInfo2::GetCodecInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3 Interface</a>
 

 

