---
UID: NN:wmsdkidl.IWMProfileManager
title: IWMProfileManager (wmsdkidl.h)
description: The IWMProfileManager interface is used to create profiles, load existing profiles, and save profiles.
helpviewer_keywords: ["IWMProfileManager","IWMProfileManager interface [windows Media Format]","IWMProfileManager interface [windows Media Format]","described","IWMProfileManagerInterface","wmformat.iwmprofilemanager","wmsdkidl/IWMProfileManager"]
old-location: wmformat\iwmprofilemanager.htm
tech.root: wmformat
ms.assetid: e5ec945c-4513-48ad-8bef-e0fb54826991
ms.date: 4/26/2023
ms.keywords: IWMProfileManager, IWMProfileManager interface [windows Media Format], IWMProfileManager interface [windows Media Format],described, IWMProfileManagerInterface, wmformat.iwmprofilemanager, wmsdkidl/IWMProfileManager
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMProfileManager
 - wmsdkidl/IWMProfileManager
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProfileManager
---

# IWMProfileManager interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMProfileManager</b> interface is used to create profiles, load existing profiles, and save profiles. It can be used with both system profiles and application-defined custom profiles. To make changes to a profile, you must load it into a profile object using one of the loading methods of this interface. You can then access the profile data through the use of the interfaces of the profile object.

<b>IWMProfileManager</b> is the default interface of a profile manager object. When you create a new profile manager object using the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager">WMCreateProfileManager</a> function, you obtain a pointer to <b>IWMProfileManager</b>.

<div class="alert"><b>Note</b>  When a profile manager object is created it parses all of the system profiles. Creating and releasing a profile manager every time you need to use it will adversely affect performance. You should create a profile manager once in your application and release it only when you no longer need to use it.</div>
<div> </div>

## -inheritance

The <b>IWMProfileManager</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMProfileManager</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2">IWMProfileManager2 Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="/windows/desktop/wmformat/profile-object">Profile Object</a>



<a href="/windows/desktop/wmformat/using-system-profiles">Using System Profiles</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
