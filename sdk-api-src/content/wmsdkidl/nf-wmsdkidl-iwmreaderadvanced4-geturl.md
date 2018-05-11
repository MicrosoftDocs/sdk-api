---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetURL
title: IWMReaderAdvanced4::GetURL
author: windows-driver-content
description: The GetURL method retrieves the URL of the file being read. This URL might be different from the URL that was passed to IWMReader::Open, because the reader might have been redirected.
old-location: wmformat\iwmreaderadvanced4_geturl.htm
old-project: wmformat
ms.assetid: 1c17be57-da35-40f2-a216-97d6953c7311
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetURL, GetURL method [windows Media Format], GetURL method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetURL method, IWMReaderAdvanced4.GetURL, IWMReaderAdvanced4::GetURL, IWMReaderAdvanced4GetURL, wmformat.iwmreaderadvanced4_geturl, wmsdkidl/IWMReaderAdvanced4::GetURL
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced4.GetURL
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced4::GetURL


## -description



The <b>GetURL</b> method retrieves the URL of the file being read. This URL might be different from the URL that was passed to <a href="https://msdn.microsoft.com/ab5b7f9e-b647-4121-abb3-2c9deb1f50cc">IWMReader::Open</a>, because the reader might have been redirected.




## -parameters




### -param pwszURL

[ out ] Pointer to a wide-character <b>null</b>-terminated string containing the URL of the file.


### -param pcchURL [in]

[ in, out ] Pointer to a variable containing the number of wide characters in <i>pwszURL</i>.


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
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



Call this method twice. The first time, pass <b>NULL</b> as the value for <i>pwszURL</i>. The method returns the size of the string in the <i>pcchURL</i> parameter. Allocate the required amount of memory for the string and call the method again. This time, pass a pointer to the allocated buffer in the <i>pwszURL</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/56695c57-f6c5-4c57-b3d4-73d169b379fa">IWMReaderAdvanced4 Interface</a>
 

 

