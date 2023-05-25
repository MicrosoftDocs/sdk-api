---
UID: NN:wmsdkidl.IWMProfileManagerLanguage
title: IWMProfileManagerLanguage (wmsdkidl.h)
description: The IWMProfileManagerLanguage interface controls the language of the system profiles parsed by the profile manager.An IWMProfileManagerLanguage interface exists for every profile manager object.
helpviewer_keywords: ["IWMProfileManagerLanguage","IWMProfileManagerLanguage interface [windows Media Format]","IWMProfileManagerLanguage interface [windows Media Format]","described","IWMProfileManagerLanguageInterface","wmformat.iwmprofilemanagerlanguage","wmsdkidl/IWMProfileManagerLanguage"]
old-location: wmformat\iwmprofilemanagerlanguage.htm
tech.root: wmformat
ms.assetid: 54875162-65fe-4959-b567-38c17ba2894d
ms.date: 4/26/2023
ms.keywords: IWMProfileManagerLanguage, IWMProfileManagerLanguage interface [windows Media Format], IWMProfileManagerLanguage interface [windows Media Format],described, IWMProfileManagerLanguageInterface, wmformat.iwmprofilemanagerlanguage, wmsdkidl/IWMProfileManagerLanguage
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
 - IWMProfileManagerLanguage
 - wmsdkidl/IWMProfileManagerLanguage
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
 - IWMProfileManagerLanguage
---

# IWMProfileManagerLanguage interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMProfileManagerLanguage</b> interface controls the language of the system profiles parsed by the profile manager.

An <b>IWMProfileManagerLanguage</b> interface exists for every profile manager object. You can obtain a pointer to an instance of this method by calling the <b>QueryInterface</b> method of any other interface of the profile manager object.

## -inheritance

The <b>IWMProfileManagerLanguage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMProfileManagerLanguage</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
