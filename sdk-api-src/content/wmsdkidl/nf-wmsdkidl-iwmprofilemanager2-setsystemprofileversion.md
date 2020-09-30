---
UID: NF:wmsdkidl.IWMProfileManager2.SetSystemProfileVersion
title: IWMProfileManager2::SetSystemProfileVersion (wmsdkidl.h)
description: The SetSystemProfileVersion method specifies the version number of the system profiles that the profile manager enumerates.
helpviewer_keywords: ["IWMProfileManager2 interface [windows Media Format]","SetSystemProfileVersion method","IWMProfileManager2.SetSystemProfileVersion","IWMProfileManager2::SetSystemProfileVersion","IWMProfileManager2SetSystemProfileVersion","SetSystemProfileVersion","SetSystemProfileVersion method [windows Media Format]","SetSystemProfileVersion method [windows Media Format]","IWMProfileManager2 interface","wmformat.iwmprofilemanager2_setsystemprofileversion","wmsdkidl/IWMProfileManager2::SetSystemProfileVersion"]
old-location: wmformat\iwmprofilemanager2_setsystemprofileversion.htm
tech.root: wmformat
ms.assetid: cd957f3b-401c-4ab1-9c54-7b4ac895caac
ms.date: 12/05/2018
ms.keywords: IWMProfileManager2 interface [windows Media Format],SetSystemProfileVersion method, IWMProfileManager2.SetSystemProfileVersion, IWMProfileManager2::SetSystemProfileVersion, IWMProfileManager2SetSystemProfileVersion, SetSystemProfileVersion, SetSystemProfileVersion method [windows Media Format], SetSystemProfileVersion method [windows Media Format],IWMProfileManager2 interface, wmformat.iwmprofilemanager2_setsystemprofileversion, wmsdkidl/IWMProfileManager2::SetSystemProfileVersion
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
 - IWMProfileManager2::SetSystemProfileVersion
 - wmsdkidl/IWMProfileManager2::SetSystemProfileVersion
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
 - IWMProfileManager2.SetSystemProfileVersion
---

# IWMProfileManager2::SetSystemProfileVersion


## -description

The <b>SetSystemProfileVersion</b> method specifies the version number of the system profiles that the profile manager enumerates.

## -parameters

### -param dwVersion

One member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_version">WMT_VERSION</a> enumeration type.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.

WMT_VER_4_0 is the default for backward-compatibility only, so be sure to set this to a newer version if it is required. Typically you should set this to WMT_VER_8_0 in order to retrieve the version 8 profiles to use as a starting point for creating your own Windows Media 9 Series profile. If you set it to WMT_VER_9_0, zero profiles will be enumerated.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2">IWMProfileManager2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofilemanager2-getsystemprofileversion">IWMProfileManager2::GetSystemProfileVersion</a>