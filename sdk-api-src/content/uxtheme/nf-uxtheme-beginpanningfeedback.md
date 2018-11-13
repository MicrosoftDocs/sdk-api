---
UID: NF:uxtheme.BeginPanningFeedback
title: BeginPanningFeedback function
author: windows-sdk-content
description: Must be called on a window to use the UpdatePanningFeedback method for boundary feedback.
old-location: wintouch\setpanningfeedback.htm
tech.root: wintouch
ms.assetid: 97956666-c875-4417-a7d1-8818871408a0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BeginPanningFeedback, BeginPanningFeedback function [Windows Touch], uxtheme/BeginPanningFeedback, wintouch.setpanningfeedback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: uxtheme.h
req.include-header: Uxtheme.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - BeginPanningFeedback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BeginPanningFeedback function


## -description


Must be
  called on a window to use the <a href="https://msdn.microsoft.com/ae316f16-e443-4d7e-bb8a-fff6ba495111">UpdatePanningFeedback</a> method for boundary feedback.
  


## -parameters




### -param hwnd [in]

A handle to the window that will have boundary feedback on it.


## -returns



Indicates whether the function was successful.




## -remarks



Panning feedback causes the window that is being manipulated to have a visual cue when a user reaches 
       the end of a pannable area.  The window may also give the user feedback if they attempt to drag it beyond the pannable region.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &amp;si);
        yPos = si.nPos;

        ZeroMemory(&amp;gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &amp;gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &amp;si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &amp;si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags &amp; GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags &amp; GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos &gt;= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags &amp; GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr &gt; 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/4d02d124-7f7a-4bda-90af-d8d19e45a09e">EndPanningFeedback</a>



<a href="https://msdn.microsoft.com/7872a4cb-6ae0-449a-866a-58f909b6ef9f">Functions</a>



<a href="https://msdn.microsoft.com/eb01a6df-9969-44d1-a657-4f83fb0b67cb">Improving the Single Finger Panning Experience</a>



<a href="https://msdn.microsoft.com/ae316f16-e443-4d7e-bb8a-fff6ba495111">UpdatePanningFeedback</a>
 

 

