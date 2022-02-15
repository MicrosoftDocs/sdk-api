---
UID: NF:shobjidl_core.ITaskbarList3.ThumbBarSetImageList
title: ITaskbarList3::ThumbBarSetImageList (shobjidl_core.h)
description: Specifies an image list that contains button images for a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","ThumbBarSetImageList method","ITaskbarList3.ThumbBarSetImageList","ITaskbarList3::ThumbBarSetImageList","ThumbBarSetImageList","ThumbBarSetImageList method [Windows Shell]","ThumbBarSetImageList method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_ThumbBarSetImageList","shell.ITaskbarList3_ThumbBarSetImageList","shobjidl_core/ITaskbarList3::ThumbBarSetImageList"]
old-location: shell\ITaskbarList3_ThumbBarSetImageList.htm
tech.root: shell
ms.assetid: 5c288b64-8630-42ca-9821-8e131f11f76d
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],ThumbBarSetImageList method, ITaskbarList3.ThumbBarSetImageList, ITaskbarList3::ThumbBarSetImageList, ThumbBarSetImageList, ThumbBarSetImageList method [Windows Shell], ThumbBarSetImageList method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_ThumbBarSetImageList, shell.ITaskbarList3_ThumbBarSetImageList, shobjidl_core/ITaskbarList3::ThumbBarSetImageList
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList3::ThumbBarSetImageList
 - shobjidl_core/ITaskbarList3::ThumbBarSetImageList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList3.ThumbBarSetImageList
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Applications must provide these button images:
                
                


<ul>
<li>The button in its default active state.</li>
<li>Images suitable for use with high-dpi (dots per inch) displays.</li>
</ul>


Images must be 32-bit and of dimensions <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_CXICON) x <a href="/windows/desktop/api/winuser/nf-winuser-getsystemmetrics">GetSystemMetrics</a>(SM_CYICON). The toolbar itself provides visuals for a button's clicked, disabled, and hover states.


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

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons">ITaskbarList3::ThumbBarAddButtons</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ITaskbarList3::ThumbBarUpdateButtons</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>