---
UID: NF:wmsdkidl.IWMStreamConfig3.SetLanguage
title: IWMStreamConfig3::SetLanguage
author: windows-sdk-content
description: The SetLanguage method sets the language for a stream using an RFC1766-compliant string.
old-location: wmformat\iwmstreamconfig3_setlanguage.htm
old-project: wmformat
ms.assetid: 3d5c65b1-5e8b-4ee7-b28c-a35376c91ac4
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMStreamConfig3 interface [windows Media Format],SetLanguage method, IWMStreamConfig3.SetLanguage, IWMStreamConfig3::SetLanguage, IWMStreamConfig3SetLanguage, SetLanguage, SetLanguage method [windows Media Format], SetLanguage method [windows Media Format],IWMStreamConfig3 interface, wmformat.iwmstreamconfig3_setlanguage, wmsdkidl/IWMStreamConfig3::SetLanguage
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMStreamConfig3.SetLanguage
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



The string passed to this method must be an RFC1766-compliant string. Use of other strings will cause problems when streaming a file made with this profile. For a list of commonly used language strings, see <a href="https://msdn.microsoft.com/625f7e95-0d21-4e16-8323-0f6301a04b30">Language Strings</a>.

The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681">IWMStreamConfig3 Interface</a>



<a href="https://msdn.microsoft.com/407607c8-c6ab-4400-b86c-9972d95f90c2">IWMStreamConfig3::GetLanguage</a>
 

 

