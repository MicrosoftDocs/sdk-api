---
UID: NE:mfplay._MFP_CREATION_OPTIONS
title: MFP_CREATION_OPTIONS (mfplay.h)
description: Specifies options for the MFPCreateMediaPlayer function.
helpviewer_keywords: ["MFP_OPTION_FREE_THREADED_CALLBACK","MFP_OPTION_NONE","MFP_OPTION_NO_MMCSS","MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION","_MFP_CREATION_OPTIONS","_MFP_CREATION_OPTIONS enumeration [Media Foundation]","mf._mfp_creation_options","mfplay/MFP_OPTION_FREE_THREADED_CALLBACK","mfplay/MFP_OPTION_NONE","mfplay/MFP_OPTION_NO_MMCSS","mfplay/MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION","mfplay/_MFP_CREATION_OPTIONS"]
old-location: mf\_mfp_creation_options.htm
tech.root: mf
ms.assetid: e01b402c-e21e-4db0-b933-5a32fdca5d2f
ms.date: 12/05/2018
ms.keywords: MFP_OPTION_FREE_THREADED_CALLBACK, MFP_OPTION_NONE, MFP_OPTION_NO_MMCSS, MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION, _MFP_CREATION_OPTIONS, _MFP_CREATION_OPTIONS enumeration [Media Foundation], mf._mfp_creation_options, mfplay/MFP_OPTION_FREE_THREADED_CALLBACK, mfplay/MFP_OPTION_NONE, mfplay/MFP_OPTION_NO_MMCSS, mfplay/MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION, mfplay/_MFP_CREATION_OPTIONS
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: _MFP_CREATION_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MFP_CREATION_OPTIONS
 - mfplay/_MFP_CREATION_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - _MFP_CREATION_OPTIONS
---

# _MFP_CREATION_OPTIONS enumeration


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Specifies options for the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a> function.

## -enum-fields

### -field MFP_OPTION_NONE:0

Use the default creation options.

### -field MFP_OPTION_FREE_THREADED_CALLBACK:0x1

If set, the MFPlay player object invokes the application's <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a> callback on another thread, and not the thread that called the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a> function. Therefore, the callback must be thread safe.

If this flag is not set, the player object invokes the callback on the same thread that calls <a href="/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a>. This thread must have a message loop. Internally, the player object creates a hidden window to dispatch the callback, similar to the mechanism used for single-threaded apartments (STAs) in COM.

### -field MFP_OPTION_NO_MMCSS:0x2

Do not register the playback topology with the Multimedia Class Scheduler Service (MMCSS). By default, the MFPlay object registers the playback topology with MMCSS, which typically results in a better playback experience. For more information, see <a href="/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices">IMFWorkQueueServices</a>.

### -field MFP_OPTION_NO_REMOTE_DESKTOP_OPTIMIZATION:0x4

Disables optimizations that are otherwise performed when the application runs in a Remote Desktop Services (RDS, formerly Terminal Services) environment.

## -remarks

The following <b>typedef</b> is defined for combining flags from this enumeration.


``` syntax
typedef UINT32 MFP_CREATION_OPTIONS;
```


## -see-also

<a href="/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
