---
UID: NF:vpconfig.IVPBaseConfig.GetConnectInfo
title: IVPBaseConfig::GetConnectInfo (vpconfig.h)
description: The GetConnectInfo method retrieves information about the connections supported by the VPE object.
helpviewer_keywords: ["GetConnectInfo","GetConnectInfo method [DirectShow]","GetConnectInfo method [DirectShow]","IVPBaseConfig interface","IVPBaseConfig interface [DirectShow]","GetConnectInfo method","IVPBaseConfig.GetConnectInfo","IVPBaseConfig::GetConnectInfo","IVPBaseConfigGetConnectInfo","dshow.ivpbaseconfig_getconnectinfo","vpconfig/IVPBaseConfig::GetConnectInfo"]
old-location: dshow\ivpbaseconfig_getconnectinfo.htm
tech.root: dshow
ms.assetid: b428e77a-83c3-42ce-95e4-1cdde4da066d
ms.date: 4/26/2023
ms.keywords: GetConnectInfo, GetConnectInfo method [DirectShow], GetConnectInfo method [DirectShow],IVPBaseConfig interface, IVPBaseConfig interface [DirectShow],GetConnectInfo method, IVPBaseConfig.GetConnectInfo, IVPBaseConfig::GetConnectInfo, IVPBaseConfigGetConnectInfo, dshow.ivpbaseconfig_getconnectinfo, vpconfig/IVPBaseConfig::GetConnectInfo
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IVPBaseConfig::GetConnectInfo
 - vpconfig/IVPBaseConfig::GetConnectInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.GetConnectInfo
---

# IVPBaseConfig::GetConnectInfo


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetConnectInfo</code> method retrieves information about the connections supported by the VPE object.

## -parameters

### -param pdwNumConnectInfo [in, out]

Pointer to a variable that specifies the number of <b>DDVIDEOPORTCONNECT</b> structures in the <i>pddVPConnectInfo</i> array. On input, specifies the size of the array (in number of array elements). On output, contains the actual number of <b>DDVIDEOPORTCONNECT</b> structures that were copied into the array. If <i>pddVPConnectInfo</i> is <b>NULL</b>, the method returns the required array size.

### -param pddVPConnectInfo [in, out]

Pointer to an array of <b>DDVIDEOPORTCONNECT</b> structures, allocated by the caller. The device fills in the array with the connection information.

## -returns

Returns S_OK if successful, or an error code otherwise.

## -remarks

The client first calls this method with the value <b>NULL</b> for the <i>pddVPConnectInfo</i> parameter. The device returns the number of <b>DDVIDEOPORTCONNECT</b> structures in the <i>pdwNumConnectInfo</i> parameter. The client allocates an array of that size, and calls the method again, passing the address of the array in the <i>pddVPConnectInfo</i> parameter. The device copies the connection information into the buffer, and returns the actual number of copied structures in the <i>pdwNumConnectInfo</i> parameter.

The <b>DDVIDEOPORTCONNECT</b> structure is documented in the Windows DDK. The device can translate this method directly into an <i>DdVideoPortGetConnectInfo</i> call.

The client sets the connection information by calling the <a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-setconnectinfo">IVPBaseConfig::SetConnectInfo</a> method with an index number, which references one of the connection structures returned by this method.

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>