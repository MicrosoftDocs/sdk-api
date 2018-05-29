---
UID: NF:winuser.TOUCH_COORD_TO_PIXEL
title: TOUCH_COORD_TO_PIXEL macro
author: windows-sdk-content
description: Converts touch coordinates to pixels.
old-location: wintouch\touch_coord_to_pixel.htm
old-project: wintouch
ms.assetid: 719b6800-aeda-424a-86ea-d8c307bd6ad2
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: TOUCH_COORD_TO_PIXEL, TOUCH_COORD_TO_PIXEL macro [Windows Touch], wintouch.touch_coord_to_pixel, winuser/TOUCH_COORD_TO_PIXEL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: winuser.h
req.include-header: Windows.h
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	winuser.h
api_name:
-	TOUCH_COORD_TO_PIXEL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# TOUCH_COORD_TO_PIXEL macro


## -description


Converts touch coordinates to pixels.


## -parameters




### -param l

The value to be converted from touch coordinates to pixels.


## -remarks




  The <b>TOUCH_COORD_TO_PIXEL</b> macro is used to convert from touch coordinates (currently centipixels) to pixels. 
  Touch coordinates are finer grained than pixels so that application developers can use subpixel granularity
  for specialized applications such as graphic design.
  


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i &lt; static_cast&lt;INT&gt;(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 &amp;&amp; index &lt; MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &amp;ptInput);
          
          if (ti.dwFlags &amp; TOUCHEVENTF_UP){                      
            points[index][0] = -1;
            points[index][1] = -1;                
          }else{
            points[index][0] = ptInput.x;
            points[index][1] = ptInput.y;                
          }
        }
      }
    }
    // If you handled the message and don't want anything else done with it, you can close it
    CloseTouchInputHandle((HTOUCHINPUT)lParam);
    delete [] pInputs;
  }else{
    // Handle the error here 
  }  
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3f10887f-5679-43b6-8bd0-f30e3bf715a1">Macros</a>
 

 

