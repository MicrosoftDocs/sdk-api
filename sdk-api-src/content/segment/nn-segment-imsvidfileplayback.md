---
UID: NN:segment.IMSVidFilePlayback
title: IMSVidFilePlayback (segment.h)
description: The IMSVidFilePlayback interface enables the client to specify a local file for playback. It is implemented by the MSVidFilePlaybackDevice object.
helpviewer_keywords: ["IMSVidFilePlayback","IMSVidFilePlayback interface [Microsoft TV Technologies]","IMSVidFilePlayback interface [Microsoft TV Technologies]","described","IMSVidFilePlaybackInterface","mstv.imsvidfileplayback","segment/IMSVidFilePlayback"]
old-location: mstv\imsvidfileplayback.htm
tech.root: mstv
ms.assetid: d6afaf69-5c1b-4f7f-a3cf-51268d6bc2b5
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback, IMSVidFilePlayback interface [Microsoft TV Technologies], IMSVidFilePlayback interface [Microsoft TV Technologies],described, IMSVidFilePlaybackInterface, mstv.imsvidfileplayback, segment/IMSVidFilePlayback
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IMSVidFilePlayback
 - segment/IMSVidFilePlayback
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
 - IMSVidFilePlayback
---

# IMSVidFilePlayback interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IMSVidFilePlayback</b> interface enables the client to specify a local file for playback. It is implemented by the <a href="/previous-versions/windows/desktop/mstv/msvidfileplaybackdevice">MSVidFilePlaybackDevice</a> object.

## -inheritance

The <b>IMSVidFilePlayback</b> interface inherits from <a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback</a>. <b>IMSVidFilePlayback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To play a media file using the Video Control, call the <a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-view">IMSVidCtl::View</a> method with the name of the file. The <b>View</b> method automatically loads the <a href="/previous-versions/windows/desktop/mstv/msvidfileplaybackdevice">MSVidFilePlayback</a> object.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidFilePlayback)</code>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidplayback">IMSVidPlayback</a>



<a href="/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
