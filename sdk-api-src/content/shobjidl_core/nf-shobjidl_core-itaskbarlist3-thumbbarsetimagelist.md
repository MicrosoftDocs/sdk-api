---
UID: NF:shobjidl_core.ITaskbarList3.ThumbBarSetImageList
title: ITaskbarList3::ThumbBarSetImageList
author: windows-sdk-content
description: Specifies an image list that contains button images for a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.
old-location: shell\ITaskbarList3_ThumbBarSetImageList.htm
tech.root: shell
ms.assetid: 5c288b64-8630-42ca-9821-8e131f11f76d
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],ThumbBarSetImageList method, ITaskbarList3.ThumbBarSetImageList, ITaskbarList3::ThumbBarSetImageList, ThumbBarSetImageList, ThumbBarSetImageList method [Windows Shell], ThumbBarSetImageList method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_ThumbBarSetImageList, shell.ITaskbarList3_ThumbBarSetImageList, shobjidl_core/ITaskbarList3::ThumbBarSetImageList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.ThumbBarSetImageList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskbarList3::ThumbBarSetImageList


## -description


Specifies an image list that contains button images for a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window whose thumbnail representation contains the toolbar to be updated. This handle must belong to the calling process.


### -param himl [in]

Type: <b>HIMAGELIST</b>

The handle of the image list that contains all button images to be used in the toolbar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications must provide these button images:
                
                


<ul>
<li>The button in its default active state.</li>
<li>Images suitable for use with high-dpi (dots per inch) displays.</li>
</ul>


Images must be 32-bit and of dimensions <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>(SM_CXICON) x <a href="https://msdn.microsoft.com/d063857b-6036-4e68-80af-9c70d12ae29e">GetSystemMetrics</a>(SM_CYICON). The toolbar itself provides visuals for a button's clicked, disabled, and hover states.


#### Examples

The following example shows how to create a thumbnail toolbar with two buttons whose images come from an image list.


```cpp

HRESULT AddThumbarButtons(HWND hwnd, HIMAGELIST himl, HIMAGELIST himlHot)
{
    // Define an array of two buttons. These buttons provide images through an 
    // image list and also provide tooltips.
    DWORD dwMask = THB_BITMAP | THB_TOOLTIP | THB_FLAGS;
    
    THUMBBUTON thbButtons[2];
    thbButtons[0].dwMask = dwMask;
    thbButtons[0].iId = 0;
    thbButtons[0].iBitmap = 0;
    thbButtons[0].pszTip = TEXT("Button 1");
    thbButtons[0].dwFlags = THBF_DISMISSONCLICK;

    dwMask = THB_BITMAP | THB_TOOLTIP;
    thbButtons[1].dwMask = dwMask;
    thbButtons[1].iId = 1;
    thbButtons[1].iBitmap = 1;
    thbButtons[1].pszTip = TEXT("Button 2");
    
    // Create an instance of ITaskbarList3
    ITaskBarList3 *ptbl;
    HRESULT hr = CoCreateInstance(CLSID_TaskbarList, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&ptbl);

    if (SUCCEEDED(hr))
    {
        // Declare the image list that contains the button images.
        hr = ptbl->ThumbBarSetImageList(hwnd, himl);
        
        if (SUCCEEDED(hr))
        {
            // Attach the toolbar to the thumbnail.
            hr = ptbl->ThumbBarAddButtons(hwnd, ARRAYSIZE(thbButtons), &thbButtons);
        }
        ptbl->Release();
    }
    return hr;
}
```





## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/5d573879-aa90-41d9-a9b7-b813dafa78ae">ITaskbarList3::ThumbBarAddButtons</a>



<a href="https://msdn.microsoft.com/5bb38b1e-dc09-4868-b424-f11beca6e64f">ITaskbarList3::ThumbBarUpdateButtons</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

