---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0004_0001
title: VMR9AspectRatioMode (vmr9.h)
description: The VMR9AspectRatioMode enumeration type is used with the IVMRWindowlessControl9::GetAspectRatioMode and IVMRWindowlessControl9::SetAspectRatioMode methods to set and retrieve the aspect ratio mode (VMR-9 only).
helpviewer_keywords: ["VMR9ARMode_LetterBox","VMR9ARMode_None","VMR9AspectRatioMode","VMR9AspectRatioMode","VMR9AspectRatioMode enumeration [DirectShow]","VMR9AspectRatioModeEnumeration","dshow.vmr9aspectratiomode","vmr9/VMR9ARMode_LetterBox","vmr9/VMR9ARMode_None","vmr9/VMR9AspectRatioMode"]
old-location: dshow\vmr9aspectratiomode.htm
tech.root: dshow
ms.assetid: 745e7aad-a598-4be6-b28b-bb5969ef0c77
ms.date: 4/26/2023
ms.keywords: VMR9ARMode_LetterBox, VMR9ARMode_None, VMR9AspectRatioMode, VMR9AspectRatioMode , VMR9AspectRatioMode enumeration [DirectShow], VMR9AspectRatioModeEnumeration, dshow.vmr9aspectratiomode, vmr9/VMR9ARMode_LetterBox, vmr9/VMR9ARMode_None, vmr9/VMR9AspectRatioMode
req.header: vmr9.h
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
req.typenames: VMR9AspectRatioMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0004_0001
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0004_0001
 - VMR9AspectRatioMode
 - vmr9/VMR9AspectRatioMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9AspectRatioMode
---

# VMR9AspectRatioMode enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9AspectRatioMode</code> enumeration type is used with the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-getaspectratiomode">IVMRWindowlessControl9::GetAspectRatioMode</a> and <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrwindowlesscontrol9-setaspectratiomode">IVMRWindowlessControl9::SetAspectRatioMode</a> methods to set and retrieve the aspect ratio mode (VMR-9 only).

## -enum-fields

### -field VMR9ARMode_None:0

Indicates that the VMR is not attempting to maintain the aspect ratio of the source video.

### -field VMR9ARMode_LetterBox

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
