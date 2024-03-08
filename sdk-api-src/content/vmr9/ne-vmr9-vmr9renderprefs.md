---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0008_0001
title: VMR9RenderPrefs (vmr9.h)
description: The VMR9RenderPrefs enumeration type specifies basic rendering preferences for the VMR-9. It is used with the IVMRFilterConfig9::GetRenderingPrefs and IVMRFilterConfig9::SetRenderingPrefs methods.
helpviewer_keywords: ["RenderPrefs9_DoNotRenderBorder","RenderPrefs9_Mask","VMR9RenderPrefs","VMR9RenderPrefs","VMR9RenderPrefs enumeration [DirectShow]","VMR9RenderPrefsEnumeration","dshow.vmr9renderprefs","vmr9/RenderPrefs9_DoNotRenderBorder","vmr9/RenderPrefs9_Mask","vmr9/VMR9RenderPrefs"]
old-location: dshow\vmr9renderprefs.htm
tech.root: dshow
ms.assetid: a32119c2-a10d-41a0-b3e9-500323eb3094
ms.date: 4/26/2023
ms.keywords: RenderPrefs9_DoNotRenderBorder, RenderPrefs9_Mask, VMR9RenderPrefs, VMR9RenderPrefs , VMR9RenderPrefs enumeration [DirectShow], VMR9RenderPrefsEnumeration, dshow.vmr9renderprefs, vmr9/RenderPrefs9_DoNotRenderBorder, vmr9/RenderPrefs9_Mask, vmr9/VMR9RenderPrefs
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
req.typenames: VMR9RenderPrefs
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0008_0001
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0008_0001
 - VMR9RenderPrefs
 - vmr9/VMR9RenderPrefs
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
 - VMR9RenderPrefs
---

# VMR9RenderPrefs enumeration


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>VMR9RenderPrefs</code> enumeration type specifies basic rendering preferences for the VMR-9. It is used with the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-getrenderingprefs">IVMRFilterConfig9::GetRenderingPrefs</a> and <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingprefs">IVMRFilterConfig9::SetRenderingPrefs</a> methods.

## -enum-fields

### -field RenderPrefs9_DoNotRenderBorder:0x1

Indicates that the application paints the color keyed areas.

### -field RenderPrefs9_Mask:0x1

Bitwise <b>OR</b> of all flags; not used by applications.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
