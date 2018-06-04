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

# ITaskbarList3::ThumbBarUpdateButtons


## -description


Shows, enables, disables, or hides buttons in a thumbnail toolbar as required by the window's current state. A thumbnail toolbar is a toolbar embedded in a thumbnail image of a window in a taskbar button flyout.


## -parameters




### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window whose thumbnail representation contains the toolbar.


### -param cButtons [in]

Type: <b>UINT</b>

The number of buttons defined in the array pointed to by <i>pButton</i>. The maximum number of buttons allowed is 7. This array contains only structures that represent existing buttons that are being updated.


### -param pButton [in]

Type: <b>LPTHUMBBUTTON</b>

A pointer to an array of <a href="https://msdn.microsoft.com/c13657b2-5b96-45ae-b339-b06b13aca65d">THUMBBUTTON</a> structures. Each <b>THUMBBUTTON</b> defines an individual button. If the button already exists (the <b>iId</b> value is already defined), then that existing button is updated with the information provided in the structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Because there is a limited amount of space in which to display thumbnails, as well as a constantly changing number of thumbnails to display, applications are not guaranteed a specific toolbar size. If display space is low, buttons in the toolbar are truncated from right to left as needed. Therefore, an application should prioritize the commands associated with its buttons to ensure that those of highest priority are to the left and are therefore least likely to be truncated.

Thumbnail toolbars are displayed only when thumbnails are being displayed on the taskbar. For instance, if a taskbar button represents a group with more open windows than there is room to display thumbnails for, the UI reverts to a legacy menu rather than thumbnails.


#### Examples

The following example shows how to use <b>ThumbBarUpdateButtons</b> to change the text and image on an existing button in a thumbnail toolbar on the extended taskbar.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT UpdateThumbarButton(HWND hwnd)
{
    // Define a single structure for the button to update. The ID is that
    // of an existing button, so the other information (bitmap index and 
    // tooltip) overwrites the existing values, updating the button.
    THUMBBUTON thbButton;
    thbButton.dwMask = THB_BITMAP | THB_TOOLTIP;
    thbButtons[0].iId = 1;
    thbButton.iBitmap = 3;
    thbButton.pszTip = TEXT("Different Text");
    
    // Create an instance of ITaskbarList3
    ITaskBarList3 *ptbl;
    HRESULT hr = CoCreateInstance(CLSID_TaskbarList, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&amp;ptbl);

    if (SUCCEEDED(hr))
    {
        // Update the toolbar. In this case, only the single button is updated.
        hr = ptbl-&gt;ThumbBarUpdateButtons(hwnd, 1, &amp;thbButton);
        ptbl-&gt;Release();
    }
    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/c63f5fe8-4a8f-4ca8-bd6a-7733110bbb38">ITaskbarList</a>



<a href="https://msdn.microsoft.com/8af23586-349f-4d21-98cb-0aaa27a586ff">ITaskbarList2</a>



<a href="https://msdn.microsoft.com/a5eb4e5a-df17-4aca-96fb-d8475e266b92">ITaskbarList3</a>



<a href="https://msdn.microsoft.com/5d573879-aa90-41d9-a9b7-b813dafa78ae">ITaskbarList3::ThumbBarAddButtons</a>



<a href="https://msdn.microsoft.com/5c288b64-8630-42ca-9821-8e131f11f76d">ITaskbarList3::ThumbBarSetImageList</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

