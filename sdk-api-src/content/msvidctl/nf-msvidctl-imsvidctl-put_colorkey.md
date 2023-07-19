---
UID: NF:msvidctl.IMSVidCtl.put_ColorKey
title: IMSVidCtl::put_ColorKey (msvidctl.h)
description: The put_ColorKey method specifies the color key.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","put_ColorKey method","IMSVidCtl.put_ColorKey","IMSVidCtl::put_ColorKey","IMSVidCtlput_ColorKey","mstv.imsvidctl_put_colorkey","msvidctl/IMSVidCtl::put_ColorKey","put_ColorKey","put_ColorKey method [Microsoft TV Technologies]","put_ColorKey method [Microsoft TV Technologies]","IMSVidCtl interface"]
old-location: mstv\imsvidctl_put_colorkey.htm
tech.root: mstv
ms.assetid: 2896f062-4ff9-4652-89b9-5fe55c6fe472
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],put_ColorKey method, IMSVidCtl.put_ColorKey, IMSVidCtl::put_ColorKey, IMSVidCtlput_ColorKey, mstv.imsvidctl_put_colorkey, msvidctl/IMSVidCtl::put_ColorKey, put_ColorKey, put_ColorKey method [Microsoft TV Technologies], put_ColorKey method [Microsoft TV Technologies],IMSVidCtl interface
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
 - IMSVidCtl::put_ColorKey
 - msvidctl/IMSVidCtl::put_ColorKey
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
 - IMSVidCtl.put_ColorKey
---

# IMSVidCtl::put_ColorKey


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_ColorKey</b> method specifies the color key.

## -parameters

### -param NewValue [in]

Specifies the color key as an <b>OLE_COLOR</b> value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The color key is used when the video renderer draws to an overlay surface.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-get_colorkey">IMSVidCtl::get_ColorKey</a>