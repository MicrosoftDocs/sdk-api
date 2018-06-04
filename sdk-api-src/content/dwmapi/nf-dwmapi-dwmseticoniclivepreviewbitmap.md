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

# DwmSetIconicLivePreviewBitmap function


## -description


Sets a static, iconic bitmap to display a <i>live preview</i> (also known as a <i>Peek preview</i>) of a window or tab. The taskbar can use this bitmap to show a full-sized preview of a window or tab.


## -parameters




### -param hwnd

A handle to the window. This window must belong to the calling process.


### -param hbmp

A handle to the bitmap to represent the window that <i>hwnd</i> specifies.


### -param pptClient [in, optional]

The offset of a tab window's <i>client region</i> (the content area inside the client window frame) from the host window's frame. This offset enables the tab window's contents to be drawn correctly in a live preview  when it is drawn without its frame.


### -param dwSITFlags

The display options for the live preview. This parameter can be 0 or the following value.



#### DWM_SIT_DISPLAYFRAME (0x00000001)

0x00000001. Displays a frame around the provided bitmap.


## -returns



Returns <b>S_OK</b> if the function succeeds, or an error value otherwise. Note that because this bitmap is not cached, if the window is not being previewed when an application calls this function, the function returns a success code but the bitmap is discarded and not used.




## -remarks



A <i>live preview</i> (also known as a <i>Peek preview</i>) of a window appears when a user moves the mouse pointer over the window's thumbnail in the taskbar or gives the thumbnail focus in the ALT+TAB window. This view is a full-sized view of the window and can be a snapshot or an iconic representation.

A window typically calls the <b>DwmSetIconicLivePreviewBitmap</b> function in response to a <a href="https://msdn.microsoft.com/24bf3b42-a850-4aa5-966a-29baab6b4d21">WM_DWMSENDICONICLIVEPREVIEWBITMAP</a> message. The returned bitmap must not be larger than the client area of the window or frame and must have 32-bit color depth.

The Desktop Window Manager (DWM) uses a copy of the bitmap, but the caller retains ownership of the original bitmap and is responsible for freeing the resources that it uses when it is no longer needed. The DWM does not keep its copy of the bitmap when the DWM stops displaying the live preview representation.


#### Examples

 To set a static, iconic bitmap to use as a live preview for the application's window, an application calls the <b>DwmSetIconicLivePreviewBitmap</b> function. To set this bitmap, the application must call <a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a> to set window attributes for non-client rendering to  <b>DWMWA_FORCE_ICONIC_REPRESENTATION</b> and <b>DWMWA_HAS_ICONIC_BITMAP</b>,  as shown in the following code. 

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>            // Set DWM window attributes to provide the iconic bitmap, and 
            // to always render the thumbnail using the iconic bitmap.
            BOOL fForceIconic = TRUE;
            BOOL fHasIconicBitmap = TRUE;

            DwmSetWindowAttribute(
                hwnd,
                DWMWA_FORCE_ICONIC_REPRESENTATION,
                &amp;fForceIconic,
                sizeof(fForceIconic));

            DwmSetWindowAttribute(
                hwnd,
                DWMWA_HAS_ICONIC_BITMAP,
                &amp;fHasIconicBitmap,
                sizeof(fHasIconicBitmap));
</pre>
</td>
</tr>
</table></span></div>
Then, the application calls <b>DwmSetIconicLivePreviewBitmap</b>  to respond to the <a href="https://msdn.microsoft.com/24bf3b42-a850-4aa5-966a-29baab6b4d21">WM_DWMSENDICONICLIVEPREVIEWBITMAP</a> message, as shown in the following code.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>        case WM_DWMSENDICONICLIVEPREVIEWBITMAP:
        {
            // This window is being asked to provide a bitmap to show in Peek preview.
            // This indicates the thumbnail in the taskbar is being previewed.
            RECT rectWindow = {0, 0, 0, 0};
            if (GetClientRect(hwnd, &amp;rectWindow))
            {
                nWidth = rectWindow.right - rectWindow.left;
                nHeight = rectWindow.bottom - rectWindow.top;
            }

            hbm = CreateDIB(nWidth, nHeight);
            if (hbm)
            {
                hr = DwmSetIconicLivePreviewBitmap(hwnd, hbm, NULL, DWM_SIT_DISPLAYFRAME);
                DeleteObject(hbm);
            }
        }
        break;
</pre>
</td>
</tr>
</table></span></div>
For the complete example, see the  <a href="https://msdn.microsoft.com/43fe71e7-4e5c-46fb-876b-e26996071665">Customize an Iconic Thumbnail and a Live Preview Bitmap</a> sample.



