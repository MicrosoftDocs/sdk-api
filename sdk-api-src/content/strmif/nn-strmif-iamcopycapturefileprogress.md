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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
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
            *ppv = static_cast&lt;IUnknown*&gt;(this);
        }
        else if (iid == IID_IAMCopyCaptureFileProgress) 
        {
            *ppv = static_cast&lt;IAMCopyCaptureFileProgress*&gt;(this);
        }
        else
        {
            return E_NOINTERFACE;
        }
        return S_OK;
    }
    STDMETHODIMP Progress(int iPercent) 
    {
        if (iPercent &lt; 0 || iPercent &gt; 100) 
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
</pre>
</td>
</tr>
</table></span></div>
The following example uses this class in the <b>CopyCaptureFile</b> method:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
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
    hr = pBuilder-&gt;CopyCaptureFile(szCaptureFile, szDestFile, TRUE,
        static_cast&lt;IAMCopyCaptureFileProgress*&gt;(&amp;Prog));
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

