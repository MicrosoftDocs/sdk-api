---
UID: NN:wmsdkidl.IWMProfile
title: IWMProfile (wmsdkidl.h)
description: The IWMProfile interface is the primary interface for a profile object.
helpviewer_keywords: ["IWMProfile","IWMProfile interface [windows Media Format]","IWMProfile interface [windows Media Format]","described","IWMProfileInterface","wmformat.iwmprofile","wmsdkidl/IWMProfile"]
old-location: wmformat\iwmprofile.htm
tech.root: wmformat
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
ms.date: 12/05/2018
ms.keywords: IWMProfile, IWMProfile interface [windows Media Format], IWMProfile interface [windows Media Format],described, IWMProfileInterface, wmformat.iwmprofile, wmsdkidl/IWMProfile
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
 - IWMProfile
 - wmsdkidl/IWMProfile
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
 - IWMProfile
---

# IWMProfile interface


## -description

The <b>IWMProfile</b> interface is the primary interface for a <a href="/windows/desktop/wmformat/wmformat-glossary">profile</a> object. A profile object is used to configure custom profiles. You can use <b>IWMProfile</b> to create, delete, or modify stream configuration objects and mutual exclusion objects. You can also set and retrieve general information about the profile. To access all the features of the profile object, you should use <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>, which inherits from <b>IWMProfile</b> and <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>.

<b>IWMProfile</b> is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader. When accessing <b>IWMProfile</b> from the reader, you can make changes to the profile, but none of the changes can be saved to the file. It is often handy to use the profile of an existing file as the foundation of a new profile. The synchronous reader supports <b>IWMProfile</b> in the same way as the reader.

The profile information obtained through the reader or synchronous reader does not come from a .prx file. The reader uses the information in the ASF file to assemble the stream configurations. Thus certain profile information, like the name and description, are not available through the reader.

There are several ways to obtain a pointer to an <b>IWMProfile</b> interface. The profile manager has methods to create a new profile and to access existing profiles. All of these methods set an <b>IWMProfile</b> pointer. When reading a file, a pointer to <b>IWMProfile</b> can be obtained by calling the <b>QueryInterface</b> method of any reader interface. Likewise, any interface of the synchronous reader object can obtain a pointer with a call to <b>QueryInterface</b><a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>.

## -inheritance

The <b>IWMProfile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMProfile</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>
