---
UID: NN:wmsdkidl.IWMMutualExclusion
title: IWMMutualExclusion (wmsdkidl.h)
description: The IWMMutualExclusion interface represents a group of streams, of which only one at a time can be played.IWMMutualExclusion is the base interface for mutual exclusion objects.
helpviewer_keywords: ["IWMMutualExclusion","IWMMutualExclusion interface [windows Media Format]","IWMMutualExclusion interface [windows Media Format]","described","IWMMutualExclusionInterface","wmformat.iwmmutualexclusion","wmsdkidl/IWMMutualExclusion"]
old-location: wmformat\iwmmutualexclusion.htm
tech.root: wmformat
ms.assetid: 040635fb-de00-4c8c-9c39-c28c409311c3
ms.date: 12/05/2018
ms.keywords: IWMMutualExclusion, IWMMutualExclusion interface [windows Media Format], IWMMutualExclusion interface [windows Media Format],described, IWMMutualExclusionInterface, wmformat.iwmmutualexclusion, wmsdkidl/IWMMutualExclusion
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
 - IWMMutualExclusion
 - wmsdkidl/IWMMutualExclusion
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
 - IWMMutualExclusion
---

# IWMMutualExclusion interface


## -description

The <b>IWMMutualExclusion</b> interface represents a group of streams, of which only one at a time can be played.

<b>IWMMutualExclusion</b> is the base interface for mutual exclusion objects. You can create a mutual exclusion object only as part of a profile. Never use COM functions, such as <b>CoCreateInstance</b>, to create a mutual exclusion object. Instead, you must already have a profile opened and make a call to its <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion">IWMProfile::CreateNewMutualExclusion</a> method. After a mutual exclusion object has been created, you can change the type of mutual exclusion by using the methods in this interface.

You can manage the streams in a mutual exclusion object using the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a> interface. <b>IWMMutualExclusion</b> inherits from <b>IWMStreamList</b>, so those methods are directly available in this interface.

## -inheritance

The <b>IWMMutualExclusion</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>. <b>IWMMutualExclusion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>



<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>
