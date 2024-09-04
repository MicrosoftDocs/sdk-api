---
UID: NN:strmif.IAMCopyCaptureFileProgress
title: IAMCopyCaptureFileProgress (strmif.h)
description: The IAMCopyCaptureFileProgress interface is a callback interface used by the ICaptureGraphBuilder2::CopyCaptureFile method.Because the CopyCaptureFile method can take a long time to complete, an application can implement this interface to receive periodic notifications about the progress of the copy operation. If the application does not need to receive this information, there is no need to implement the interface.
helpviewer_keywords: ["IAMCopyCaptureFileProgress","IAMCopyCaptureFileProgress interface [DirectShow]","IAMCopyCaptureFileProgress interface [DirectShow]","described","IAMCopyCaptureFileProgressInterface","dshow.iamcopycapturefileprogress","strmif/IAMCopyCaptureFileProgress"]
old-location: dshow\iamcopycapturefileprogress.htm
tech.root: dshow
ms.assetid: 780ffe63-f4b6-4b3c-b7a6-571b58aba4dd
ms.date: 4/26/2023
ms.keywords: IAMCopyCaptureFileProgress, IAMCopyCaptureFileProgress interface [DirectShow], IAMCopyCaptureFileProgress interface [DirectShow],described, IAMCopyCaptureFileProgressInterface, dshow.iamcopycapturefileprogress, strmif/IAMCopyCaptureFileProgress
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMCopyCaptureFileProgress
 - strmif/IAMCopyCaptureFileProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMCopyCaptureFileProgress
---

# IAMCopyCaptureFileProgress interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IAMCopyCaptureFileProgress</code> interface is a callback interface used by the <a href="/windows/desktop/api/strmif/nf-strmif-icapturegraphbuilder2-copycapturefile">ICaptureGraphBuilder2::CopyCaptureFile</a> method.

Because the <b>CopyCaptureFile</b> method can take a long time to complete, an application can implement this interface to receive periodic notifications about the progress of the copy operation. If the application does not need to receive this information, there is no need to implement the interface.

## -inheritance

The <b>IAMCopyCaptureFileProgress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAMCopyCaptureFileProgress</b> also has these types of members:

## -remarks

To use this interface, implement a class that inherits the interface and implements all of its methods, including the methods in <b>IUnknown</b>. In your application, create an instance of the class and pass it to the <b>CopyCaptureFile</b> method. You do not have to implement COM reference counting in your class, as long as the object is guaranteed not to be deleted before the <b>CopyCaptureFile</b> method returns.

The following example shows a class that implements the interface:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>

```
class CProgress : public IAMCopyCaptureFileProgress 
{
public:
    STDMETHODIMP_(ULONG) AddRef() { return 1; }
    STDMETHODIMP_(ULONG) Release() { return 0; }
    STDMETHODIMP QueryInterface(REFIID iid, void **ppv) 
    {
        if  (ppv == NULL) 
        {
            return E_POINTER;
        }
        else if (iid == __uuidof(IUnknown))
        {
            *ppv = static_cast<IUnknown*>(this);
        }
        else if (iid == IID_IAMCopyCaptureFileProgress) 
        {
            *ppv = static_cast<IAMCopyCaptureFileProgress*>(this);
        }
        else
        {
            return E_NOINTERFACE;
        }
        return S_OK;
    }
    STDMETHODIMP Progress(int iPercent) 
    {
        if (iPercent < 0 || iPercent > 100) 
        {
            return E_INVALIDARG;
        }

        TCHAR szMsg[32];
        StringCchPrintf(szMsg, 32, TEXT("Progress: %d%%"), iPercent);
        // Assume g_hwndStatus is a valid HWND.
        SetWindowText(g_hwndStatus, szMsg);  

        return S_OK;
    };
};
```
</td>
</tr>
</table></span></div>
The following example uses this class in the <b>CopyCaptureFile</b> method:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Scope for CProgress object
{
    CProgress Prog;
    // Assume pBuilder is an initialized ICaptureGraphBuilder2 pointer.
    hr = pBuilder->CopyCaptureFile(szCaptureFile, szDestFile, TRUE,
        static_cast<IAMCopyCaptureFileProgress*>(&amp;Prog));
}
</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>
