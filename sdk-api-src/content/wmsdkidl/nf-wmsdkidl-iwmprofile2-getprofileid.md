---
UID: NF:wmsdkidl.IWMProfile2.GetProfileID
title: IWMProfile2::GetProfileID
author: windows-sdk-content
description: The GetProfileID method retrieves the globally unique identifier of a system profile.
old-location: wmformat\iwmprofile2_getprofileid.htm
old-project: wmformat
ms.assetid: 82e3e086-4b19-4eb9-91ad-d30392f97a28
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: GetProfileID, GetProfileID method [windows Media Format], GetProfileID method [windows Media Format],IWMProfile2 interface, GetProfileID method [windows Media Format],IWMProfile3 interface, IWMProfile2 interface [windows Media Format],GetProfileID method, IWMProfile2.GetProfileID, IWMProfile2::GetProfileID, IWMProfile2GetProfileID, IWMProfile3 interface [windows Media Format],GetProfileID method, IWMProfile3::GetProfileID, wmformat.iwmprofile2_getprofileid, wmsdkidl/IWMProfile2::GetProfileID, wmsdkidl/IWMProfile3::GetProfileID
ms.prod: windows
ms.technology: windows-sdk
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
 - qasf.dll
api_name:
 - IWMProfile2.GetProfileID
 - IWMProfile3.GetProfileID
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



System profiles have associated identifiers, but custom profiles do not, therefore this method cannot be used to identify any profile that uses the Windows Media® 9 Series codecs. For more information, see <a href="https://msdn.microsoft.com/e2263c3a-56cd-4505-acd7-510dc7bac166">Reusing Stream Configurations</a>.




## -see-also




<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2 Interface</a>



<a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>
 

 

