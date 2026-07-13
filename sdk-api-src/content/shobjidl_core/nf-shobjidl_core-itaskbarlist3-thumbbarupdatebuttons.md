---
UID: NF:shobjidl_core.ITaskbarList3.ThumbBarUpdateButtons
title: ITaskbarList3::ThumbBarUpdateButtons (shobjidl_core.h)
description: Shows, enables, disables, or hides buttons in a thumbnail toolbar as required by the window's current state. A thumbnail toolbar is a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.
helpviewer_keywords: ["ITaskbarList3 interface [Windows Shell]","ThumbBarUpdateButtons method","ITaskbarList3.ThumbBarUpdateButtons","ITaskbarList3::ThumbBarUpdateButtons","ThumbBarUpdateButtons","ThumbBarUpdateButtons method [Windows Shell]","ThumbBarUpdateButtons method [Windows Shell]","ITaskbarList3 interface","_shell_ITaskbarList3_ThumbBarUpdateButtons","shell.ITaskbarList3_ThumbBarUpdateButtons","shobjidl_core/ITaskbarList3::ThumbBarUpdateButtons"]
old-location: shell\ITaskbarList3_ThumbBarUpdateButtons.htm
tech.root: shell
ms.assetid: 5bb38b1e-dc09-4868-b424-f11beca6e64f
ms.date: 08/22/2025
ms.keywords: ITaskbarList3 interface [Windows Shell],ThumbBarUpdateButtons method, ITaskbarList3.ThumbBarUpdateButtons, ITaskbarList3::ThumbBarUpdateButtons, ThumbBarUpdateButtons, ThumbBarUpdateButtons method [Windows Shell], ThumbBarUpdateButtons method [Windows Shell],ITaskbarList3 interface, _shell_ITaskbarList3_ThumbBarUpdateButtons, shell.ITaskbarList3_ThumbBarUpdateButtons, shobjidl_core/ITaskbarList3::ThumbBarUpdateButtons
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
 - ITaskbarList3::ThumbBarUpdateButtons
 - shobjidl_core/ITaskbarList3::ThumbBarUpdateButtons
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
 - ITaskbarList3.ThumbBarUpdateButtons
---

# ITaskbarList3::ThumbBarUpdateButtons

## -description

Shows, enables, disables, or hides buttons in a thumbnail toolbar as required by the window's current state. A thumbnail toolbar is a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.

## -parameters

### -param hwnd [in]

Type: **HWND**

The handle of the window whose thumbnail representation contains the toolbar.

### -param cButtons [in]

Type: **UINT**

The number of buttons defined in the array pointed to by _pButton_. The maximum number of buttons allowed is 7. This array contains only structures that represent existing buttons that are being updated.

### -param pButton [in]

Type: **LPTHUMBBUTTON**

A pointer to an array of [THUMBBUTTON](ns-shobjidl_core-thumbbutton.md) structures. Each **THUMBBUTTON** defines an individual button. If the button already exists (the **iId** value is already defined), then that existing button is updated with the information provided in the structure.

## -returns

Type: **HRESULT**

If this method succeeds, it returns **S_OK**. Otherwise, it returns an **HRESULT** error code.

## -remarks

Because there is a limited amount of space in which to display thumbnails, as well as a constantly changing number of thumbnails to display, applications are not guaranteed a specific toolbar size. If display space is low, buttons in the toolbar are truncated from right to left as needed. Therefore, an application should prioritize the commands associated with its buttons to ensure that those of highest priority are to the left and are therefore least likely to be truncated.

Thumbnail toolbars are displayed only when thumbnails are being displayed on the taskbar. For instance, if a taskbar button represents a group with more open windows than there is room to display thumbnails for, the UI reverts to a legacy menu rather than thumbnails.

### Accessibility

For information about accessibility in thumb bar button images, see the Remarks section of [ThumbBarSetImageList](nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist.md).

### Examples

The following example shows how to use **ThumbBarUpdateButtons** to change the text and image on an existing button in a thumbnail toolbar on the extended taskbar.


```cpp
HRESULT UpdateThumbBarButton(HWND hwnd)
{
    // Define a single structure for the button to update. The ID is that
    // of an existing button, so the other information (bitmap index and 
    // tooltip) overwrites the existing values, updating the button.
    THUMBBUTTON thbButton;
    thbButton.dwMask = THB_BITMAP | THB_TOOLTIP;
    thbButtons[0].iId = 1;
    thbButton.iBitmap = 3;
    thbButton.pszTip = TEXT("Different Text");
    
    // Create an instance of ITaskbarList3
    ITaskBarList3 *ptbl;
    HRESULT hr = CoCreateInstance(CLSID_TaskbarList, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&ptbl);

    if (SUCCEEDED(hr))
    {
        // Update the toolbar. In this case, only the single button is updated.
        hr = ptbl->ThumbBarUpdateButtons(hwnd, 1, &thbButton);
        ptbl->Release();
    }
    return hr;
}
```

## -see-also

[ITaskbarList](nn-shobjidl_core-itaskbarlist.md)

[ITaskbarList2](nn-shobjidl_core-itaskbarlist2.md)

[ITaskbarList3](nn-shobjidl_core-itaskbarlist3.md)

[ITaskbarList3::ThumbBarSetImageList](nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist.md)

[ITaskbarList3::ThumbBarAddButtons](nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons.md)

[Taskbar Extensions](/windows/desktop/shell/taskbar-extensions)
