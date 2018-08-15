---
UID: NF:wmsdkidl.IWMVideoMediaProps.GetQuality
title: IWMVideoMediaProps::GetQuality
author: windows-sdk-content
description: The GetQuality method retrieves the quality setting for the video stream.
old-location: wmformat\iwmvideomediaprops_getquality.htm
old-project: wmformat
ms.assetid: 9edfe229-ffc5-4266-93af-1938bbd577c2
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetQuality, GetQuality method [windows Media Format], GetQuality method [windows Media Format],IWMVideoMediaProps interface, IWMVideoMediaProps interface [windows Media Format],GetQuality method, IWMVideoMediaProps.GetQuality, IWMVideoMediaProps::GetQuality, IWMVideoMediaPropsGetQuality, wmformat.iwmvideomediaprops_getquality, wmsdkidl/IWMVideoMediaProps::GetQuality
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
api_name:
 - IWMVideoMediaProps.GetQuality
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMVideoMediaProps::GetQuality


## -description



The <b>GetQuality</b> method retrieves the quality setting for the video stream.




## -parameters




### -param pdwQuality [out]

Pointer to a <b>DWORD</b> containing the quality setting.


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
<i>pdwQuality</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information, see the Remarks for <a href="https://msdn.microsoft.com/0f91380d-b8c8-47db-99ca-12c897bdff20">SetQuality</a>.




## -see-also




<a href="https://msdn.microsoft.com/4d6ba1d8-b046-450b-a3f9-4810faba5b77">IWMVideoMediaProps Interface</a>
 

 

