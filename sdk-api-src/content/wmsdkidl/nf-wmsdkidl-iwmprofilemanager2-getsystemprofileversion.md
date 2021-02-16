---
UID: NF:wmsdkidl.IWMProfileManager2.GetSystemProfileVersion
title: IWMProfileManager2::GetSystemProfileVersion (wmsdkidl.h)
description: The GetSystemProfileVersion method retrieves the version number of the system profiles that the profile manager enumerates.
helpviewer_keywords: ["GetSystemProfileVersion","GetSystemProfileVersion method [windows Media Format]","GetSystemProfileVersion method [windows Media Format]","IWMProfileManager2 interface","IWMProfileManager2 interface [windows Media Format]","GetSystemProfileVersion method","IWMProfileManager2.GetSystemProfileVersion","IWMProfileManager2::GetSystemProfileVersion","IWMProfileManager2GetSystemProfileVersion","wmformat.iwmprofilemanager2_getsystemprofileversion","wmsdkidl/IWMProfileManager2::GetSystemProfileVersion"]
old-location: wmformat\iwmprofilemanager2_getsystemprofileversion.htm
tech.root: wmformat
ms.assetid: 155b847b-81c0-4065-ae00-ca0b64cdd537
ms.date: 12/05/2018
ms.keywords: GetSystemProfileVersion, GetSystemProfileVersion method [windows Media Format], GetSystemProfileVersion method [windows Media Format],IWMProfileManager2 interface, IWMProfileManager2 interface [windows Media Format],GetSystemProfileVersion method, IWMProfileManager2.GetSystemProfileVersion, IWMProfileManager2::GetSystemProfileVersion, IWMProfileManager2GetSystemProfileVersion, wmformat.iwmprofilemanager2_getsystemprofileversion, wmsdkidl/IWMProfileManager2::GetSystemProfileVersion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMProfileManager2::GetSystemProfileVersion
 - wmsdkidl/IWMProfileManager2::GetSystemProfileVersion
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
 - IWMProfileManager2.GetSystemProfileVersion
---

# IWMProfileManager2::GetSystemProfileVersion


## -description

The <b>GetSystemProfileVersion</b> method retrieves the version number of the system profiles that the profile manager enumerates.

## -parameters

### -param pdwVersion

Pointer to one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_version">WMT_VERSION</a> enumeration type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2">IWMProfileManager2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager2-setsystemprofileversion">IWMProfileManager2::SetSystemProfileVersion</a>