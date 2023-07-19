---
UID: NF:msvidctl.IMSVidCtl.get_ColorKey
title: IMSVidCtl::get_ColorKey (msvidctl.h)
description: The get_ColorKey method retrieves the color key that the video renderer is using.
helpviewer_keywords: ["IMSVidCtl interface [Microsoft TV Technologies]","get_ColorKey method","IMSVidCtl.get_ColorKey","IMSVidCtl::get_ColorKey","IMSVidCtlget_ColorKey","get_ColorKey","get_ColorKey method [Microsoft TV Technologies]","get_ColorKey method [Microsoft TV Technologies]","IMSVidCtl interface","mstv.imsvidctl_get_colorkey","msvidctl/IMSVidCtl::get_ColorKey"]
old-location: mstv\imsvidctl_get_colorkey.htm
tech.root: mstv
ms.assetid: 2f197faf-a91e-4984-8858-ceab6506b273
ms.date: 12/05/2018
ms.keywords: IMSVidCtl interface [Microsoft TV Technologies],get_ColorKey method, IMSVidCtl.get_ColorKey, IMSVidCtl::get_ColorKey, IMSVidCtlget_ColorKey, get_ColorKey, get_ColorKey method [Microsoft TV Technologies], get_ColorKey method [Microsoft TV Technologies],IMSVidCtl interface, mstv.imsvidctl_get_colorkey, msvidctl/IMSVidCtl::get_ColorKey
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
 - IMSVidCtl::get_ColorKey
 - msvidctl/IMSVidCtl::get_ColorKey
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
 - IMSVidCtl.get_ColorKey
---

# IMSVidCtl::get_ColorKey


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ColorKey</b> method retrieves the color key that the video renderer is using.

## -parameters

### -param CurrentValue [out]

Receives an <b>OLE_COLOR</b> value.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The color key is used when the video renderer draws to an overlay surface.


#### Examples


```cpp

OLE_COLOR ocKey;
COLORREF clrKey;
pVideoControl->get_ColorKey(&ocKey);
OleTranslateColor(ocKey, 0, &clrKey);
```

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidctl">IMSVidCtl Interface</a>



<a href="/previous-versions/windows/desktop/api/msvidctl/nf-msvidctl-imsvidctl-put_colorkey">IMSVidCtl::put_ColorKey</a>



<a href="/windows/desktop/api/strmif/nf-strmif-ivmrwindowlesscontrol-getcolorkey">IVMRWindowlessControl::GetColorKey</a>