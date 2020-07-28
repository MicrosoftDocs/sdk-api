---
UID: NF:wmsdkidl.IWMHeaderInfo.AddScript
title: IWMHeaderInfo::AddScript (wmsdkidl.h)
description: The AddScript method adds a script, consisting of type and command strings, and a specific time, to the header section of the ASF file.
helpviewer_keywords: ["AddScript","AddScript method [windows Media Format]","AddScript method [windows Media Format]","IWMHeaderInfo interface","AddScript method [windows Media Format]","IWMHeaderInfo2 interface","AddScript method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","AddScript method","IWMHeaderInfo.AddScript","IWMHeaderInfo2 interface [windows Media Format]","AddScript method","IWMHeaderInfo2::AddScript","IWMHeaderInfo3 interface [windows Media Format]","AddScript method","IWMHeaderInfo3::AddScript","IWMHeaderInfo::AddScript","IWMHeaderInfoAddScript","wmformat.iwmheaderinfo_addscript","wmsdkidl/IWMHeaderInfo2::AddScript","wmsdkidl/IWMHeaderInfo3::AddScript","wmsdkidl/IWMHeaderInfo::AddScript"]
old-location: wmformat\iwmheaderinfo_addscript.htm
tech.root: wmformat
ms.assetid: e20644fb-077e-4eee-8802-6099002f3969
ms.date: 12/05/2018
ms.keywords: AddScript, AddScript method [windows Media Format], AddScript method [windows Media Format],IWMHeaderInfo interface, AddScript method [windows Media Format],IWMHeaderInfo2 interface, AddScript method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],AddScript method, IWMHeaderInfo.AddScript, IWMHeaderInfo2 interface [windows Media Format],AddScript method, IWMHeaderInfo2::AddScript, IWMHeaderInfo3 interface [windows Media Format],AddScript method, IWMHeaderInfo3::AddScript, IWMHeaderInfo::AddScript, IWMHeaderInfoAddScript, wmformat.iwmheaderinfo_addscript, wmsdkidl/IWMHeaderInfo2::AddScript, wmsdkidl/IWMHeaderInfo3::AddScript, wmsdkidl/IWMHeaderInfo::AddScript
f1_keywords:
- wmsdkidl/IWMHeaderInfo.AddScript
dev_langs:
- c++
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
- IWMHeaderInfo.AddScript
- IWMHeaderInfo2.AddScript
- IWMHeaderInfo3.AddScript
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMHeaderInfo::AddScript


## -description



The <b>AddScript</b> method adds a script, consisting of type and command strings, and a specific time, to the header section of the ASF file. 




## -parameters




### -param pwszType [in]

Pointer to a wide-character null-terminated string containing the type. Script types are limited to 1024 wide characters.


### -param pwszCommand [in]

Pointer to a wide-character null-terminated string containing the command. Script commands are limited to 10240 wide characters.


### -param cnsScriptTime [in]

The script time in 100-nanosecond increments.


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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
No value was supplied in <i>pwszType</i> or <i>pwszCommand</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer parameter does not contain a valid pointer.

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
</table>
 




## -remarks



Before <b>BeginWriting</b> has been called, the writer only supports <b>AddScript</b>. The reader does not support <b>AddScript</b>, and always returns E_NOTIMPL.

You should not add a large number of script commands to the file header if the file is intended for streaming. Some protocols impose limits on the size of a header. Limits differ by protocol, but if your script commands total tens of kilobytes, you should create a script stream instead.

When using DRM to encrypt a file, no script command can have a presentation time of 0.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript">IWMHeaderInfo::GetScript</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removescript">IWMHeaderInfo::RemoveScript</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/using-script-commands">Using Script Commands</a>
 

 

