---
UID: NF:wmsdkidl.IWMStreamConfig3.SetLanguage
title: IWMStreamConfig3::SetLanguage (wmsdkidl.h)
author: windows-sdk-content
description: The SetLanguage method sets the language for a stream using an RFC1766-compliant string.
old-location: wmformat\iwmstreamconfig3_setlanguage.htm
tech.root: wmformat
ms.assetid: 3d5c65b1-5e8b-4ee7-b28c-a35376c91ac4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMStreamConfig3 interface [windows Media Format],SetLanguage method, IWMStreamConfig3.SetLanguage, IWMStreamConfig3::SetLanguage, IWMStreamConfig3SetLanguage, SetLanguage, SetLanguage method [windows Media Format], SetLanguage method [windows Media Format],IWMStreamConfig3 interface, wmformat.iwmstreamconfig3_setlanguage, wmsdkidl/IWMStreamConfig3::SetLanguage
ms.topic: method
f1_keywords: 
 - "wmsdkidl/IWMStreamConfig3.SetLanguage"
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
 - IWMStreamConfig3.SetLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMStreamConfig3::SetLanguage


## -description



The <b>SetLanguage</b> method sets the language for a stream using an RFC1766-compliant string.




## -parameters




### -param pwszLanguageString [in]

Pointer to a wide-character null-terminated string containing the language string.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The string passed to this method must be an RFC1766-compliant string. Use of other strings will cause problems when streaming a file made with this profile. For a list of commonly used language strings, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/language-strings">Language Strings</a>.

The new value will not take effect in the profile until you call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3">IWMStreamConfig3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-getlanguage">IWMStreamConfig3::GetLanguage</a>
 

 

