---
UID: NF:shobjidl_core.ITaskbarList3.ThumbBarAddButtons
title: ITaskbarList3::ThumbBarAddButtons (shobjidl_core.h)
description: Adds a thumbnail toolbar with a specified set of buttons to the thumbnail image of a window in a taskbar button flyout.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","ThumbBarAddButtons method","ITaskbarList3.ThumbBarAddButtons","ITaskbarList3::ThumbBarAddButtons","ThumbBarAddButtons","ThumbBarAddButtons method [Windows Shell]","ThumbBarAddButtons method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_ThumbBarAddButtons","shell.ITaskbarList3_ThumbBarAddButtons","shobjidl_core/ITaskbarList3::ThumbBarAddButtons"]
old-location: shell\ITaskbarList3_ThumbBarAddButtons.htm
tech.root: shell
ms.assetid: 5d573879-aa90-41d9-a9b7-b813dafa78ae
ms.date: 12/05/2018
ms.keywords: ITaskbarList3 interface [Windows Shell],ThumbBarAddButtons method, ITaskbarList3.ThumbBarAddButtons, ITaskbarList3::ThumbBarAddButtons, ThumbBarAddButtons, ThumbBarAddButtons method [Windows Shell], ThumbBarAddButtons method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_ThumbBarAddButtons, shell.ITaskbarList3_ThumbBarAddButtons, shobjidl_core/ITaskbarList3::ThumbBarAddButtons
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
 - ITaskbarList3::ThumbBarAddButtons
 - shobjidl_core/ITaskbarList3::ThumbBarAddButtons
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
 - ITaskbarList3.ThumbBarAddButtons
---

# ITaskbarList3::ThumbBarAddButtons


## -description

Adds a thumbnail toolbar with a specified set of buttons to the thumbnail image of a window in a taskbar button flyout.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window whose thumbnail representation will receive the toolbar. This handle must belong to the calling process.

### -param cButtons [in]

Type: <b>UINT</b>

The number of buttons defined in the array pointed to by <i>pButton</i>. The maximum number of buttons allowed is 7.

### -param pButton [in]

Type: <b>LPTHUMBBUTTON</b>

A pointer to an array of <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a> structures. Each <b>THUMBBUTTON</b> defines an individual button to be added to the toolbar. Buttons cannot be added or deleted later, so this must be the full defined set. Buttons also cannot be reordered, so their order in the array, which is the order in which they are displayed left to right, will be their permanent order.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>hwnd</i> parameter does not specify a handle that belongs to the process or does not specify a window that is associated with a taskbar button. This value is also returned if <i>pButton</i> is less than 1 or greater than 7.

</td>
</tr>
</table>

## -remarks

This method allows an application to define buttons for an active toolbar control that is embedded in a window's taskbar thumbnail preview. This provides access to the window's essential commands without making the user restore or activate the window. For example, Windows Media Player might offer standard media transport controls such as play, pause, mute, and stop.

The toolbar used in the thumbnail is essentially a standard <a href="/windows/desktop/Controls/toolbar-control-reference">toolbar</a> control. It has a maximum of seven buttons, and it is center-aligned, transparent, and displayed in an area beneath the thumbnail rather than covering any portion of it. Each button's ID, image, tooltip, and state are defined in a <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a> structure, which is then passed to the taskbar. The application can then subsequently show, alter, or hide buttons from the thumbnail toolbar as required by its current state by calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ITaskbarList3::ThumbBarUpdateButtons</a>.

When a button in a thumbnail toolbar is clicked, the window associated with that thumbnail is sent a <a href="/windows/desktop/menurc/wm-command">WM_COMMAND</a> message with the <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> of its <i>wParam</i> parameter set to <b>THBN_CLICKED</b> and the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> to the button ID.

After a toolbar has been added to a thumbnail, buttons can be altered only through <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ITaskbarList3::ThumbBarUpdateButtons</a>. While individual buttons cannot be added or removed, they can be shown and hidden through <b>ThumbBarUpdateButtons</b> as needed. The toolbar itself cannot be removed without re-creating the window itself.

Because there is a limited amount of space in which to display thumbnails, as well as a constantly changing number of thumbnails to display, applications are not guaranteed a specific toolbar size. If display space is low, buttons in the toolbar are truncated from right to left as needed. Therefore, an application should prioritize the commands associated with its buttons to ensure that those of highest priority are to the left and are therefore least likely to be truncated.

Thumbnail toolbars are displayed only when thumbnails are being displayed. For instance, if a taskbar button represents a group with more open windows than there is room to display thumbnails for, the UI reverts to a legacy menu rather than thumbnails.


#### Examples

The following example shows how to use <b>ThumbBarAddButtons</b> to add a toolbar that contains two buttons to a thumbnail on the extended taskbar.


```cpp
HRESULT AddThumbarButtons(HWND hwnd, HIMAGELIST himl, HIMAGELIST himlHot)
{
    // Define an array of two buttons. These buttons provide images through an 
    // image list and also provide tooltips.
    DWORD dwMask = THB_BITMAP | THB_TOOLTIP | THB_FLAGS;
    
    THUMBBUTTON thbButtons[2];
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



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist">ITaskbarList3::ThumbBarSetImageList</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarupdatebuttons">ITaskbarList3::ThumbBarUpdateButtons</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>