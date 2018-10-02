---
UID: NF:wmsdkidl.IWMProfileManager2.SetSystemProfileVersion
title: IWMProfileManager2::SetSystemProfileVersion
author: windows-sdk-content
description: The SetSystemProfileVersion method specifies the version number of the system profiles that the profile manager enumerates.
old-location: wmformat\iwmprofilemanager2_setsystemprofileversion.htm
tech.root: wmformat
ms.assetid: cd957f3b-401c-4ab1-9c54-7b4ac895caac
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMProfileManager2 interface [windows Media Format],SetSystemProfileVersion method, IWMProfileManager2.SetSystemProfileVersion, IWMProfileManager2::SetSystemProfileVersion, IWMProfileManager2SetSystemProfileVersion, SetSystemProfileVersion, SetSystemProfileVersion method [windows Media Format], SetSystemProfileVersion method [windows Media Format],IWMProfileManager2 interface, wmformat.iwmprofilemanager2_setsystemprofileversion, wmsdkidl/IWMProfileManager2::SetSystemProfileVersion
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
api_name:
 - IWMProfileManager2.SetSystemProfileVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfileManager2::SetSystemProfileVersion


## -description



The <b>SetSystemProfileVersion</b> method specifies the version number of the system profiles that the profile manager enumerates.




## -parameters




### -param dwVersion

One member of the <a href="https://msdn.microsoft.com/9ee414c6-49aa-42ad-9310-52f54b23e712">WMT_VERSION</a> enumeration type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Because there are no system profiles for the Windows Media 9 Series codecs, this method is primarily useful for obtaining version 8 system profiles that you will convert to custom profiles using the Windows Media 9 Series codecs. For more information, see <a href="https://msdn.microsoft.com/e2263c3a-56cd-4505-acd7-510dc7bac166">Reusing Stream Configurations</a>.

WMT_VER_4_0 is the default for backward-compatibility only, so be sure to set this to a newer version if it is required. Typically you should set this to WMT_VER_8_0 in order to retrieve the version 8 profiles to use as a starting point for creating your own Windows Media 9 Series profile. If you set it to WMT_VER_9_0, zero profiles will be enumerated.




## -see-also




<a href="https://msdn.microsoft.com/eb5d904e-15ee-4066-ab05-c4e133bc89d7">IWMProfileManager2 Interface</a>



<a href="https://msdn.microsoft.com/155b847b-81c0-4065-ae00-ca0b64cdd537">IWMProfileManager2::GetSystemProfileVersion</a>
 

 

