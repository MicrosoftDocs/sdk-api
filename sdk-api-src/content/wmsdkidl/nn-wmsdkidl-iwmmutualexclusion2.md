---
UID: NN:wmsdkidl.IWMMutualExclusion2
title: IWMMutualExclusion2 (wmsdkidl.h)
description: The IWMMutualExclusion2 interface provides advanced configuration features for mutual exclusion objects.This interface supports both multiple languages and advanced mutual exclusion.An IWMMutualExclusion2 interface is created for each mutual exclusion object created. To retrieve a pointer to an IWMMutualExclusion2 interface, call the QueryInterface method of the IWMMutualExclusion interface returned by IWMProfile::CreateNewMutualExclusion.
helpviewer_keywords: ["IWMMutualExclusion2","IWMMutualExclusion2 interface [windows Media Format]","IWMMutualExclusion2 interface [windows Media Format]","described","IWMMutualExclusion2Interface","wmformat.iwmmutualexclusion2","wmsdkidl/IWMMutualExclusion2"]
old-location: wmformat\iwmmutualexclusion2.htm
tech.root: wmformat
ms.assetid: 4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf
ms.date: 4/26/2023
ms.keywords: IWMMutualExclusion2, IWMMutualExclusion2 interface [windows Media Format], IWMMutualExclusion2 interface [windows Media Format],described, IWMMutualExclusion2Interface, wmformat.iwmmutualexclusion2, wmsdkidl/IWMMutualExclusion2
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
 - IWMMutualExclusion2
 - wmsdkidl/IWMMutualExclusion2
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
 - IWMMutualExclusion2
---

# IWMMutualExclusion2 interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMMutualExclusion2</b> interface provides advanced configuration features for mutual exclusion objects.

This interface supports both multiple languages and advanced mutual exclusion.

An <b>IWMMutualExclusion2</b> interface is created for each mutual exclusion object created. To retrieve a pointer to an <b>IWMMutualExclusion2</b> interface, call the <b>QueryInterface</b> method of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a> interface returned by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion">IWMProfile::CreateNewMutualExclusion</a>.

## -inheritance

The <b>IWMMutualExclusion2</b> interface inherits from <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion</a>. <b>IWMMutualExclusion2</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion">IWMMutualExclusion Interface</a>



<a href="/windows/desktop/wmformat/mutual-exclusion-object">Mutual Exclusion Object</a>
