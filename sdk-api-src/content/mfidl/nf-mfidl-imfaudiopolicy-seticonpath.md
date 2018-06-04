---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFAudioPolicy::SetIconPath


## -description



          Sets the icon resource for the audio session. The Windows volume control displays this icon.
        


## -parameters




### -param pszPath [in]

A wide-character string that specifies the icon. See Remarks.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The icon path has the format "path,index" or "path,-id", where <i>path</i> is the fully qualified path to a DLL, executable file, or icon file; <i>index</i> is the zero-based index of the icon within the file; and <i>id</i> is a resource identifier. Note that resource identifiers are preceded by a minus sign (-) to distinguish them from indexes. The path can contain environment variables, such as "%windir%". For more information, see <a href="https://msdn.microsoft.com/25b27a65-7204-4a12-ae4e-ad216a22e4e1">IAudioSessionControl::SetIconPath</a> in the Windows SDK.


#### Examples

The following example sets the icon using a resource identifier for an icon in the application's executable file.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT SetIcon(IMFMediaSession *pSession, int nID)
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
        IID_PPV_ARGS(&amp;pPolicy)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPolicy-&gt;SetIconPath(szIconPath);
    if (FAILED(hr))
    {
        goto done;
    }

done:
    SafeRelease(&amp;pPolicy);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fcd4dbfb-3f9f-4089-b9cc-7b41b2c2678a">IMFAudioPolicy</a>



<a href="https://msdn.microsoft.com/5884a128-597d-432b-a706-e10c894d7965">Streaming Audio Renderer</a>
 

 

