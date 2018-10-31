---
UID: NN:strmif.IAMCopyCaptureFileProgress
title: IAMCopyCaptureFileProgress
author: windows-sdk-content
description: The IAMCopyCaptureFileProgress interface is a callback interface used by the ICaptureGraphBuilder2::CopyCaptureFile method.Because the CopyCaptureFile method can take a long time to complete, an application can implement this interface to receive periodic notifications about the progress of the copy operation. If the application does not need to receive this information, there is no need to implement the interface.
old-location: dshow\iamcopycapturefileprogress.htm
tech.root: DirectShow
ms.assetid: 780ffe63-f4b6-4b3c-b7a6-571b58aba4dd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IAMCopyCaptureFileProgress, IAMCopyCaptureFileProgress interface [DirectShow], IAMCopyCaptureFileProgress interface [DirectShow],described, IAMCopyCaptureFileProgressInterface, dshow.iamcopycapturefileprogress, strmif/IAMCopyCaptureFileProgress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMCopyCaptureFileProgress interface


## -description



The <code>IAMCopyCaptureFileProgress</code> interface is a callback interface used by the <a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">ICaptureGraphBuilder2::CopyCaptureFile</a> method.

Because the <b>CopyCaptureFile</b> method can take a long time to complete, an application can implement this interface to receive periodic notifications about the progress of the copy operation. If the application does not need to receive this information, there is no need to implement the interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMCopyCaptureFileProgress</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMCopyCaptureFileProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMCopyCaptureFileProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6908627e-51de-4206-bdb2-b3aaedf9478f">Progress</a>
</td>
<td align="left" width="63%">
Called periodically by the <a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">ICaptureGraphBuilder2::CopyCaptureFile</a> method during capture operations.

</td>
</tr>
</table> 


## -remarks



To use this interface, implement a class that inherits the interface and implements all of its methods, including the methods in <b>IUnknown</b>. In your application, create an instance of the class and pass it to the <b>CopyCaptureFile</b> method. You do not have to implement COM reference counting in your class, as long as the object is guaranteed not to be deleted before the <b>CopyCaptureFile</b> method returns.

The following example shows a class that implements the interface:


```cpp

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


The following example uses this class in the <b>CopyCaptureFile</b> method:


```cpp

// Scope for CProgress object
{
    CProgress Prog;
    // Assume pBuilder is an initialized ICaptureGraphBuilder2 pointer.
    hr = pBuilder->CopyCaptureFile(szCaptureFile, szDestFile, TRUE,
        static_cast<IAMCopyCaptureFileProgress*>(&Prog));
}

```





## -see-also




<a href="https://msdn.microsoft.com/5efd174f-2eb1-44e6-97e3-b73c7c52fef1">Interfaces</a>
 

 

