---
UID: NF:segment.IMSVidWebDVD2.get_Bookmark
title: IMSVidWebDVD2::get_Bookmark (segment.h)
description: Saves or loads the playback position and state information for a DVD.
helpviewer_keywords: ["Bookmark property [Microsoft TV Technologies]","Bookmark property [Microsoft TV Technologies]","IMSVidWebDVD2 interface","IMSVidWebDVD2 interface [Microsoft TV Technologies]","Bookmark property","IMSVidWebDVD2.Bookmark","IMSVidWebDVD2.get_Bookmark","IMSVidWebDVD2::Bookmark","IMSVidWebDVD2::get_Bookmark","IMSVidWebDVD2::put_Bookmark","get_Bookmark","mstv.imsvidwebdvd2_bookmark","segment/IMSVidWebDVD2::Bookmark","segment/IMSVidWebDVD2::get_Bookmark","segment/IMSVidWebDVD2::put_Bookmark"]
old-location: mstv\imsvidwebdvd2_bookmark.htm
tech.root: mstv
ms.assetid: e7b0f28d-16f3-4dd4-8b28-f46e492f5c8e
ms.date: 12/05/2018
ms.keywords: Bookmark property [Microsoft TV Technologies], Bookmark property [Microsoft TV Technologies],IMSVidWebDVD2 interface, IMSVidWebDVD2 interface [Microsoft TV Technologies],Bookmark property, IMSVidWebDVD2.Bookmark, IMSVidWebDVD2.get_Bookmark, IMSVidWebDVD2::Bookmark, IMSVidWebDVD2::get_Bookmark, IMSVidWebDVD2::put_Bookmark, get_Bookmark, mstv.imsvidwebdvd2_bookmark, segment/IMSVidWebDVD2::Bookmark, segment/IMSVidWebDVD2::get_Bookmark, segment/IMSVidWebDVD2::put_Bookmark
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidWebDVD2::get_Bookmark
 - segment/IMSVidWebDVD2::get_Bookmark
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidWebDVD2.Bookmark
 - IMSVidWebDVD2.get_Bookmark
 - IMSVidWebDVD2.put_Bookmark
---

# IMSVidWebDVD2::get_Bookmark


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Saves or loads the playback position and state information for a DVD.
<ul>
<li>To create a DVD bookmark and save it to a buffer, call <b>get_Bookmark</b>.</li>
<li>To load a bookmark from a buffer,  call <b>put_Bookmark</b>. Loading the bookmark restores the DVD playback state to its original state.</li>
</ul>This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidwebdvd2">IMSVidWebDVD2</a>