---
UID: NN:wmsdkidl.IWMProfile2
title: IWMProfile2 (wmsdkidl.h)
description: The IWMProfile2 interface exposes the globally unique identifier for a system profile.
helpviewer_keywords: ["IWMProfile2","IWMProfile2 interface [windows Media Format]","IWMProfile2 interface [windows Media Format]","described","IWMProfile2Interface","wmformat.iwmprofile2","wmsdkidl/IWMProfile2"]
old-location: wmformat\iwmprofile2.htm
tech.root: wmformat
ms.assetid: 34e30edb-3247-4eaa-9a63-6d94c9e37c0b
ms.date: 4/26/2023
ms.keywords: IWMProfile2, IWMProfile2 interface [windows Media Format], IWMProfile2 interface [windows Media Format],described, IWMProfile2Interface, wmformat.iwmprofile2, wmsdkidl/IWMProfile2
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
 - IWMProfile2
 - wmsdkidl/IWMProfile2
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
 - IWMProfile2
---

# IWMProfile2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMProfile2</b> interface exposes the globally unique identifier for a system profile. System profiles have associated identifiers, but custom profiles do not.

As with <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a>, <b>IWMProfile2</b> is included in profile objects as well as in reader and synchronous reader objects. To obtain a pointer to an <b>IWMProfile2</b> interface, call the <b>QueryInterface</b> method of any interface in one of these objects. For more information, see <b>IWMProfile Interface</b>.

## -inheritance

The <b>IWMProfile2</b> interface inherits from <a href="/windows/desktop/wmformat/iwmprofile">IWMProfile</a>. <b>IWMProfile2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
