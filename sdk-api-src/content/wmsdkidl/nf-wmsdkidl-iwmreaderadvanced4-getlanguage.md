---
UID: NF:wmsdkidl.IWMReaderAdvanced4.GetLanguage
title: IWMReaderAdvanced4::GetLanguage (wmsdkidl.h)
description: The GetLanguage method retrieves information about a language supported by an output. You must specify an output number and a language index, and this method will supply the RFC1766-compliant language string.
helpviewer_keywords: ["GetLanguage","GetLanguage method [windows Media Format]","GetLanguage method [windows Media Format]","IWMReaderAdvanced4 interface","IWMReaderAdvanced4 interface [windows Media Format]","GetLanguage method","IWMReaderAdvanced4.GetLanguage","IWMReaderAdvanced4::GetLanguage","IWMReaderAdvanced4GetLanguage","wmformat.iwmreaderadvanced4_getlanguage","wmsdkidl/IWMReaderAdvanced4::GetLanguage"]
old-location: wmformat\iwmreaderadvanced4_getlanguage.htm
tech.root: wmformat
ms.assetid: 2af443f5-941a-466a-8eef-d4742f8e1ae1
ms.date: 4/26/2023
ms.keywords: GetLanguage, GetLanguage method [windows Media Format], GetLanguage method [windows Media Format],IWMReaderAdvanced4 interface, IWMReaderAdvanced4 interface [windows Media Format],GetLanguage method, IWMReaderAdvanced4.GetLanguage, IWMReaderAdvanced4::GetLanguage, IWMReaderAdvanced4GetLanguage, wmformat.iwmreaderadvanced4_getlanguage, wmsdkidl/IWMReaderAdvanced4::GetLanguage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderAdvanced4::GetLanguage
 - wmsdkidl/IWMReaderAdvanced4::GetLanguage
dev_langs:
 - c++
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
 - IWMReaderAdvanced4.GetLanguage
---

# IWMReaderAdvanced4::GetLanguage


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetLanguage</b> method retrieves information about a language supported by an output. You must specify an output number and a language index, and this method will supply the RFC1766-compliant language string.

## -parameters

### -param dwOutputNum [in]

<b>DWORD</b> containing the output number for which you want to identify the language.

### -param wLanguage [in]

<b>WORD</b> containing the language index of the supported language for which you want the details.

### -param pwszLanguageString [out]

Pointer to a wide-character <b>null</b>-terminated string containing the RFC1766-compliant language string. Pass <b>NULL</b> to retrieve the size of the string, which will be returned in <i>pcbLanguageStringLength</i>.

### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the size of <i>pwszLanguageString</i> in wide characters. This size includes the terminating <b>null</b> character.

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

When setting the language to use for an output, you must set the value of the <b>g_wszLanguage</b> setting to the language index passed to this method as <i>wLanguage</i>. Do not use the language index assigned by the language list, which will be different.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4">IWMReaderAdvanced4 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount">IWMReaderAdvanced4::GetLanguageCount</a>