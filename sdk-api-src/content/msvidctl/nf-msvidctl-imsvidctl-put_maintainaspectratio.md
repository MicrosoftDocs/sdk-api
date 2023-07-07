---
UID: NF:msvidctl.IMSVidCtl.put_MaintainAspectRatio
title: IMSVidCtl::put_MaintainAspectRatio (msvidctl.h)
description: The put_MaintainAspectRatio method specifies whether the Video Control maintains the aspect ratio of the source video.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_MaintainAspectRatio method","IMSVidCtl.put_MaintainAspectRatio","IMSVidCtl::put_MaintainAspectRatio","IMSVidCtlput_MaintainAspectRatio","mstv.imsvidctl_put_maintainaspectratio","msvidctl/IMSVidCtl::put_MaintainAspectRatio","put_MaintainAspectRatio","put_MaintainAspectRatio method [Microsoft TV Technologies]","put_MaintainAspectRatio method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_maintainaspectratio.htm
tech.root: mstv
ms.assetid: 7f0943b1-3cb9-46dc-8aaf-be22e2464092
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_MaintainAspectRatio method, IMSVidCtl.put_MaintainAspectRatio, IMSVidCtl::put_MaintainAspectRatio, IMSVidCtlput_MaintainAspectRatio, mstv.imsvidctl_put_maintainaspectratio, msvidctl/IMSVidCtl::put_MaintainAspectRatio, put_MaintainAspectRatio, put_MaintainAspectRatio method [Microsoft TV Technologies], put_MaintainAspectRatio method [Microsoft TV Technologies],IMSVidCtl interface
req.header: msvidctl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msvidctl.idl
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
 - IMSVidCtl::put_MaintainAspectRatio
 - msvidctl/IMSVidCtl::put_MaintainAspectRatio
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msvidctl.h
api_name:
 - IMSVidCtl.put_MaintainAspectRatio
---

# IMSVidCtl::put_MaintainAspectRatio


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_MaintainAspectRatio</b> method specifies whether the Video Control maintains the aspect ratio of the source video.

## -parameters

### -param NewValue [in]

Specifies one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>VARIANT_TRUE</td>
<td>The Video Control will maintain the aspect ratio of the source video.</td>
</tr>
<tr>
<td>VARIANT_FALSE</td>
<td>The Video Control will stretch the video to fill the window. (Default.)</td>
</tr>
</table>

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_maintainaspectratio">IMSVidCtl::get_MaintainAspectRatio</a>