---
UID: NF:winuser.TOUCH_COORD_TO_PIXEL
title: TOUCH_COORD_TO_PIXEL macro (winuser.h)
description: Converts touch coordinates to pixels.
helpviewer_keywords: ["TOUCH_COORD_TO_PIXEL","TOUCH_COORD_TO_PIXEL macro [Windows Touch]","wintouch.touch_coord_to_pixel","winuser/TOUCH_COORD_TO_PIXEL"]
old-location: wintouch\touch_coord_to_pixel.htm
tech.root: wintouch
ms.assetid: 719b6800-aeda-424a-86ea-d8c307bd6ad2
ms.date: 07/01/2025
ms.keywords: TOUCH_COORD_TO_PIXEL, TOUCH_COORD_TO_PIXEL macro [Windows Touch], wintouch.touch_coord_to_pixel, winuser/TOUCH_COORD_TO_PIXEL
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TOUCH_COORD_TO_PIXEL
 - winuser/TOUCH_COORD_TO_PIXEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - TOUCH_COORD_TO_PIXEL
---

# TOUCH_COORD_TO_PIXEL macro

## -syntax

```cpp
long TOUCH_COORD_TO_PIXEL(
    long l
);
```

## -returns

Type: **long**

The coordinate value in pixels.


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


```cpp
case WM_TOUCH:        
  cInputs = LOWORD(wParam);
  pInputs = new TOUCHINPUT[cInputs];
  if (pInputs){
    if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
      for (int i=0; i < static_cast<INT>(cInputs); i++){
        TOUCHINPUT ti = pInputs[i];
        index = GetContactIndex(ti.dwID);
        if (ti.dwID != 0 && index < MAXPOINTS){                            
          // Do something with your touch input handle
          ptInput.x = TOUCH_COORD_TO_PIXEL(ti.x);
          ptInput.y = TOUCH_COORD_TO_PIXEL(ti.y);
          ScreenToClient(hWnd, &ptInput);
          
          if (ti.dwFlags & TOUCHEVENTF_UP){                      
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

```

## -see-also

<a href="/windows/desktop/wintouch/touch-macros">Macros</a>
