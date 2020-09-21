---
UID: NF:wmsdkidl.IWMProfile2.GetProfileID
title: IWMProfile2::GetProfileID (wmsdkidl.h)
description: The GetProfileID method retrieves the globally unique identifier of a system profile.
helpviewer_keywords: ["GetProfileID","GetProfileID method [windows Media Format]","GetProfileID method [windows Media Format]","IWMProfile2 interface","GetProfileID method [windows Media Format]","IWMProfile3 interface","IWMProfile2 interface [windows Media Format]","GetProfileID method","IWMProfile2.GetProfileID","IWMProfile2::GetProfileID","IWMProfile2GetProfileID","IWMProfile3 interface [windows Media Format]","GetProfileID method","IWMProfile3::GetProfileID","wmformat.iwmprofile2_getprofileid","wmsdkidl/IWMProfile2::GetProfileID","wmsdkidl/IWMProfile3::GetProfileID"]
old-location: wmformat\iwmprofile2_getprofileid.htm
tech.root: wmformat
ms.assetid: 82e3e086-4b19-4eb9-91ad-d30392f97a28
ms.date: 12/05/2018
ms.keywords: GetProfileID, GetProfileID method [windows Media Format], GetProfileID method [windows Media Format],IWMProfile2 interface, GetProfileID method [windows Media Format],IWMProfile3 interface, IWMProfile2 interface [windows Media Format],GetProfileID method, IWMProfile2.GetProfileID, IWMProfile2::GetProfileID, IWMProfile2GetProfileID, IWMProfile3 interface [windows Media Format],GetProfileID method, IWMProfile3::GetProfileID, wmformat.iwmprofile2_getprofileid, wmsdkidl/IWMProfile2::GetProfileID, wmsdkidl/IWMProfile3::GetProfileID
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
 - IWMProfile2::GetProfileID
 - wmsdkidl/IWMProfile2::GetProfileID
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
 - qasf.dll
api_name:
 - IWMProfile2.GetProfileID
 - IWMProfile3.GetProfileID
---

# IWMProfile2::GetProfileID


## -description

The <b>GetProfileID</b> method retrieves the globally unique identifier of a system profile.

## -parameters

### -param pguidID [out]

Pointer to a GUID specifying the ID of the profile. It the profile is not a system profile, this is set to GUID_NULL.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

System profiles have associated identifiers, but custom profiles do not, therefore this method cannot be used to identify any profile that uses the Windows Media® 9 Series codecs. For more information, see <a href="/windows/desktop/wmformat/reusing-stream-configurations">Reusing Stream Configurations</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>