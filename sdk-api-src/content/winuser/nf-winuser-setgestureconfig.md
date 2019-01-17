---
UID: NF:winuser.SetGestureConfig
title: SetGestureConfig function
author: windows-sdk-content
description: Configures the messages that are sent from a window for Windows Touch gestures.
old-location: wintouch\setgestureconfig.htm
tech.root: wintouch
ms.assetid: 7df5a18e-5e65-4dd5-a59d-853a91ead710
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetGestureConfig, SetGestureConfig function [Windows Touch], wintouch.setgestureconfig, winuser/SetGestureConfig
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
api_name:
 - SetGestureConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetGestureConfig function


## -description


Configures the messages that are sent from a window for Windows Touch gestures.
  


## -parameters




### -param hwnd [in]

A handle to the window to set the gesture configuration on.


### -param dwReserved [in]

This value is reserved and must be set to 0.


### -param cIDs [in]

A count of the gesture configuration structures that are being passed.


### -param pGestureConfig [in]

An array of gesture configuration structures that specify the gesture configuration.


### -param cbSize [in]

The size of the gesture configuration (<a href="https://msdn.microsoft.com/4ec5050e-7fef-4f52-89af-5237e8cdbdb8">GESTURECONFIG</a>) structure.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks



If you don't expect to change the gesture configuration, call <b>SetGestureConfig</b> at window creation time.
	 If you want to dynamically change the gesture configuration, call <b>SetGestureConfig</b> in response to <a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a> messages.
	 

The following table shows the identifiers for gestures that are
  supported by the <i>dwID</i> member of the <a href="https://msdn.microsoft.com/4ec5050e-7fef-4f52-89af-5237e8cdbdb8">GESTURECONFIG</a> structure.  Note that setting
  <i>dwID</i> to 0 indicates that global gesture configuration flags are set.
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GID_ZOOM</b></td>
<td>3</td>
<td>Configuration settings for the zoom gesture.</td>
</tr>
<tr>
<td><b>GID_PAN</b></td>
<td>4</td>
<td>The pan gesture.</td>
</tr>
<tr>
<td><b>GID_ROTATE</b></td>
<td>5</td>
<td>The rotation gesture.</td>
</tr>
<tr>
<td><b>GID_TWOFINGERTAP</b></td>
<td>6</td>
<td>The two-finger tap gesture.</td>
</tr>
<tr>
<td><b>GID_PRESSANDTAP</b></td>
<td>7</td>
<td>The press and tap gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to zero.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_ALLGESTURES</b></td>
<td>0x00000001</td>
<td>All of the gestures.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_ZOOM.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_ZOOM</b></td>
<td>0x00000001</td>
<td>The zoom gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to GID_PAN.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_PAN</b></td>
<td>0x00000001</td>
<td>All pan gestures.</td>
</tr>
<tr>
<td><b>GC_PAN_WITH_SINGLE_FINGER_VERTICALLY</b></td>
<td>0x00000002</td>
<td>Vertical pans with one finger.</td>
</tr>
<tr>
<td><b>GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY</b></td>
<td>0x00000004</td>
<td>Horizontal pans with one finger.</td>
</tr>
<tr>
<td><b>GC_PAN_WITH_GUTTER</b></td>
<td>0x00000008</td>
<td>Panning with a gutter boundary around the edges of pannable region.  The gutter boundary limits perpendicular movement to a primary direction until a threshold is reached to break out of the gutter.</td>
</tr>
<tr>
<td><b>GC_PAN_WITH_INTERTIA</b></td>
<td>0x00000010</td>
<td>Panning with inertia to smoothly slow when pan gestures stop.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Pan gestures can be used in conjunction with each other to control behavior. 
    For example, setting the <b>dwWant</b> bits to panning with single-finger horizontal
    and setting the <b>dwBlock</b> bits to single-finger vertical will restrict panning to horizontal pans. Changing the
    <b>dwWant</b> bit to have <code>GC_PAN_WITH_SINGLE_FINGER_VERTICALLY | GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY</code>and removing single-finger vertical pan from the <b>dwBlock </b>bit will enable both vertical and horizontal panning.    
    </div>
<div> </div>
<div class="alert"><b>Note</b>  By default, panning has inertia enabled.
    </div>
<div> </div>
<div class="alert"><b>Note</b>  A single call to <b>SetGestureConfig</b> cannot include other GIDs along with 0.	 
	 </div>
<div> </div>
The following flags are used when <i>dwID</i> is set to GID_ROTATE.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_ROTATE</b></td>
<td>0x00000001</td>
<td>The rotation gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to <b>GID_TWOFINGERTAP</b>.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_TWOFINGERTAP</b></td>
<td>0x00000001</td>
<td>The two-finger tap gesture.</td>
</tr>
</table>
 

The following flags are used when <i>dwID</i> is set to <b>GID_PRESSANDTAP</b>.

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GC_PRESSANDTAP</b></td>
<td>0x00000001</td>
<td>The press and tap gesture.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Calling <b>SetGestureConfig</b> will change the gesture configuration for the lifetime of the Window, not just for the next gesture.
	 </div>
<div> </div>

#### Examples

The following example shows how you could receive horizontal and vertical single-finger panning with no gutter and no 
		inertia. This is a typical configuration for a 2-D navigation application such as the Microsoft PixelSense Globe application.		
		


```cpp
// set up our want / block settings
DWORD dwPanWant  = GC_PAN_WITH_SINGLE_FINGER_VERTICALLY | GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY;
DWORD dwPanBlock = GC_PAN_WITH_GUTTER | GC_PAN_WITH_INERTIA;

// set the settings in the gesture configuration
GESTURECONFIG gc[] = {{ GID_ZOOM, GC_ZOOM, 0 },
                      { GID_ROTATE, GC_ROTATE, 0},
                      { GID_PAN, dwPanWant , dwPanBlock}                     
                     };    
                     
UINT uiGcs = 3;
BOOL bResult = SetGestureConfig(hWnd, 0, uiGcs, gc, sizeof(GESTURECONFIG));  

if (!bResult){                
    DWORD err = GetLastError();                                       
}

```


The following example shows how to receive single-finger pan gestures and disable gutter panning.  This is a typical
		  configuration for applications that scroll text such as Notepad.
		  

<div class="alert"><b>Note</b>  You should explicitly set all the flags that you want enabled or disabled when controlling single-finger panning.
        </div>
<div> </div>

```cpp
// set up our want / block settings
DWORD dwPanWant  = GC_PAN | GC_PAN_WITH_SINGLE_FINGER_VERTICALLY;                    
DWORD dwPanBlock = GC_PAN_WITH_GUTTER;    

// set the settings in the gesture configuration
GESTURECONFIG gc[] = {{ GID_ZOOM, GC_ZOOM, 0 },
                      { GID_ROTATE, GC_ROTATE, 0},
                      { GID_PAN, dwPanWant , dwPanBlock}                     
                     };    
                     
UINT uiGcs = 3;
BOOL bResult = SetGestureConfig(hWnd, 0, uiGcs, gc, sizeof(GESTURECONFIG));  

if (!bResult){                
    DWORD err = GetLastError();                                       
}   

```


The following example shows how you can disable all gestures.


```cpp
// set the settings in the gesture configuration
GESTURECONFIG gc[] = {0,0,GC_ALLGESTURES};
                     
UINT uiGcs = 1;
BOOL bResult = SetGestureConfig(hWnd, 0, uiGcs, gc, sizeof(GESTURECONFIG));  

if (!bResult){                
    DWORD err = GetLastError();                                       
}

```


The following example shows how you could enable all gestures.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GESTURECONFIG gc = {0,GC_ALLGESTURES,0};

UINT uiGcs = 1;

BOOL bResult = SetGestureConfig(hWnd, 0, uiGcs, &gc, sizeof(GESTURECONFIG));  

if (!bResult){                
    DWORD err = GetLastError();                                       
}              
</pre>
</td>
</tr>
</table></span></div>


The following example shows how you could enable all Windows 7 gestures.


```cpp
// set the settings in the gesture configuration
GESTURECONFIG gc[] = {{ GID_ZOOM, GC_ZOOM, 0 },
                      { GID_ROTATE, GC_ROTATE, 0},
                      { GID_PAN, GC_PAN , 0},
                      { GID_TWOFINGERTAP, GC_TWOFINGERTAP , 0},
                      { GID_PRESSANDTAP, GC_PRESSANDTAP , 0}
                     };    
                     
UINT uiGcs = 5;
BOOL bResult = SetGestureConfig(hWnd, 0, uiGcs, gc, sizeof(GESTURECONFIG));  

if (!bResult){                
    DWORD err = GetLastError();                                       
}

```


The following example configuration would set the parent window to 
		enable support for zoom, horizontal pan, and vertical pan while the child window would just support horizontal pan.

<div class="code"></div>

```cpp
// set up our want / block settings for a parent window
DWORD dwPanWant  = GC_PAN_WITH_SINGLE_FINGER_VERTICALLY | GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY;
DWORD dwPanBlock = GC_PAN_WITH_GUTTER | GC_PAN_WITH_INERTIA;

// set the settings in the gesture configuration
GESTURECONFIG gcParent[] = {{ GID_ZOOM, GC_ZOOM, 0 },
                            { GID_PAN, dwPanWant , dwPanBlock}                         
                           };    

// Set the pan settings for a child window
dwPanWant  = GC_PAN_WITH_SINGLE_FINGER_HORIZONTALLY;
dwPanBlock = GC_PAN_WITH_SINGLE_FINGER_VERTICALLY | GC_PAN_WITH_GUTTER | GC_PAN_WITH_INERTIA;
                     
GESTURECONFIG gcChild[]  = {{ GID_ZOOM, 0, GC_ZOOM },
                            { GID_PAN, dwPanWant , dwPanBlock}                         
                           };    

UINT uiGcs   = 2;
BOOL bResult = FALSE;
                     
if (isParent){      
  bResult = SetGestureConfig(hWnd, 0, uiGcs, gcParent, sizeof(GESTURECONFIG));  
}else{
  bResult = SetGestureConfig(hWnd, 0, uiGcs, gcChild, sizeof(GESTURECONFIG));  
}

if (!bResult){                
    DWORD err = GetLastError();                                       
}

```





## -see-also




<a href="https://msdn.microsoft.com/830031d1-eb8d-45d4-b66e-3f4fbb96ae13">Functions</a>



<a href="https://msdn.microsoft.com/4ec5050e-7fef-4f52-89af-5237e8cdbdb8">GESTURECONFIG</a>



<a href="https://msdn.microsoft.com/8b7a594c-e9e4-4215-8946-da170c957a2b">GetGestureConfig</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>



<a href="https://msdn.microsoft.com/83c23928-86ce-421d-bb84-5c41a770bf60">WM_GESTURENOTIFY</a>
 

 

