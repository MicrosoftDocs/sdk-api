---
UID: NN:wmsdkidl.IWMProfileManager2
title: IWMProfileManager2 (wmsdkidl.h)
description: The IWMProfileManager2 interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager.
helpviewer_keywords: ["IWMProfileManager2","IWMProfileManager2 interface [windows Media Format]","IWMProfileManager2 interface [windows Media Format]","described","IWMProfileManager2Interface","wmformat.iwmprofilemanager2","wmsdkidl/IWMProfileManager2"]
old-location: wmformat\iwmprofilemanager2.htm
tech.root: wmformat
ms.assetid: eb5d904e-15ee-4066-ab05-c4e133bc89d7
ms.date: 4/26/2023
ms.keywords: IWMProfileManager2, IWMProfileManager2 interface [windows Media Format], IWMProfileManager2 interface [windows Media Format],described, IWMProfileManager2Interface, wmformat.iwmprofilemanager2, wmsdkidl/IWMProfileManager2
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
 - IWMProfileManager2
 - wmsdkidl/IWMProfileManager2
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
 - IWMProfileManager2
---

# IWMProfileManager2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMProfileManager2</b> interface adds methods to specify and retrieve the version number of the system profiles enumerated by the profile manager. Most applications should set the value to the latest version unless they need to be backward-compatible with another application that was written using an earlier version of this SDK.

## -inheritance

The <b>IWMProfileManager2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager</a>. <b>IWMProfileManager2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
