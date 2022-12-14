---
UID: NF:mfidl.IMFAudioPolicy.SetIconPath
title: IMFAudioPolicy::SetIconPath (mfidl.h)
description: Sets the icon resource for the audio session. The Windows volume control displays this icon.
helpviewer_keywords: ["098ad6ae-b1fe-4e74-b494-572770906b14","IMFAudioPolicy interface [Media Foundation]","SetIconPath method","IMFAudioPolicy.SetIconPath","IMFAudioPolicy::SetIconPath","SetIconPath","SetIconPath method [Media Foundation]","SetIconPath method [Media Foundation]","IMFAudioPolicy interface","mf.imfaudiopolicy_seticonpath","mfidl/IMFAudioPolicy::SetIconPath"]
old-location: mf\imfaudiopolicy_seticonpath.htm
tech.root: mf
ms.assetid: 098ad6ae-b1fe-4e74-b494-572770906b14
ms.date: 12/05/2018
ms.keywords: 098ad6ae-b1fe-4e74-b494-572770906b14, IMFAudioPolicy interface [Media Foundation],SetIconPath method, IMFAudioPolicy.SetIconPath, IMFAudioPolicy::SetIconPath, SetIconPath, SetIconPath method [Media Foundation], SetIconPath method [Media Foundation],IMFAudioPolicy interface, mf.imfaudiopolicy_seticonpath, mfidl/IMFAudioPolicy::SetIconPath
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAudioPolicy::SetIconPath
 - mfidl/IMFAudioPolicy::SetIconPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioPolicy.SetIconPath
---

# IMFAudioPolicy::SetIconPath


## -description

Sets the icon resource for the audio session. The Windows volume control displays this icon.

## -parameters

### -param pszPath [in]

A wide-character string that specifies the icon. See Remarks.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The icon path has the format "path,index" or "path,-id", where <i>path</i> is the fully qualified path to a DLL, executable file, or icon file; <i>index</i> is the zero-based index of the icon within the file; and <i>id</i> is a resource identifier. Note that resource identifiers are preceded by a minus sign (-) to distinguish them from indexes. The path can contain environment variables, such as "%windir%". For more information, see <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-seticonpath">IAudioSessionControl::SetIconPath</a> in the Windows SDK.


#### Examples

The following example sets the icon using a resource identifier for an icon in the application's executable file.


```cpp
HRESULT SetIcon(IMFMediaSession *pSession, int nID)
{
    IMFAudioPolicy *pPolicy = NULL;

    const DWORD CCH_ICON_PATH = MAX_PATH + 16;
    WCHAR szFileName[MAX_PATH];
    WCHAR szIconPath[CCH_ICON_PATH];

    HRESULT hr = S_OK;

    DWORD result = GetModuleFileNameW(NULL, szFileName, MAX_PATH);

    // Note: GetModuleFileName can return a truncated string without a 
    // NULL terminator. If so, the function succeeds but sets the last 
    // error to ERROR_INSUFFICIENT_BUFFER.
    if ((result == 0) || (GetLastError() ==  ERROR_INSUFFICIENT_BUFFER))
    {
        hr = E_FAIL;
        goto done;
    }

    hr = StringCchPrintfW(szIconPath, CCH_ICON_PATH, 
                 L"%s,-%d", szFileName, nID);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFGetService(
        pSession, 
        MR_AUDIO_POLICY_SERVICE, 
        IID_PPV_ARGS(&pPolicy)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPolicy->SetIconPath(szIconPath);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&pPolicy);
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy">IMFAudioPolicy</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>