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

# tagGESTUREINFO structure


## -description


 Stores information about a gesture.


## -struct-fields




### -field cbSize

The size of the structure, in bytes. The caller must set this to <code>sizeof(GESTUREINFO)</code>.


### -field dwFlags

The state of the gesture.  For additional information, see Remarks.


### -field dwID

The identifier of the gesture command.


### -field hwndTarget

A handle to the window that is targeted by this gesture.


### -field ptsLocation

A <b>POINTS</b> structure containing the coordinates associated with the gesture. These coordinates are always relative to the origin of the screen.


### -field dwInstanceID

An internally used identifier for the structure.


### -field dwSequenceID

An internally used identifier for the sequence.


### -field ullArguments

A 64-bit unsigned integer that contains the arguments for gestures that fit into 8 bytes. 


### -field cbExtraArgs

The size, in bytes, of extra arguments that accompany this gesture.


## -remarks



The <b>HIDWORD</b> of the <b>ullArguments</b> member is always 0, with the following exceptions:

<ul>
<li>For <b>GID_PAN</b>, it is 0 except when there is inertia. When <b>GF_INERTIA</b> is set,  the <b>HIDWORD</b> is an inertia vector (two 16-bit values).</li>
<li>For <b>GID_PRESSANDTAP</b>, it is the distance between the two points.</li>
</ul>

  The <b>GESTUREINFO</b> structure is retrieved by passing the handle to the gesture information structure
  to the <a href="https://msdn.microsoft.com/407ed585-09aa-4174-8907-8bb9590f1795">GetGestureInfo</a> function.

The following flags indicate the various states of the gestures and are stored in <b>dwFlags</b>.
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>GF_BEGIN</td>
<td>0x00000001</td>
<td>A gesture is starting.</td>
</tr>
<tr>
<td>GF_INERTIA</td>
<td>0x00000002</td>
<td>A gesture has triggered inertia.</td>
</tr>
<tr>
<td>GF_END</td>
<td>0x00000004</td>
<td>A gesture has finished.</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  
  Most applications should ignore the <b>GID_BEGIN</b> and <b>GID_END</b> messages and pass them to <b>DefWindowProc</b>.  
  These messages are used by the default gesture handler. Application behavior is undefined when
  the <b>GID_BEGIN</b> and <b>GID_END</b> messages are consumed by a third-party application.</div>
<div> </div>
The following table indicates the various identifiers for gestures.
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GID_BEGIN</b></td>
<td>1</td>
<td>A gesture is starting.</td>
</tr>
<tr>
<td><b>GID_END</b></td>
<td>2</td>
<td>A gesture is ending.</td>
</tr>
<tr>
<td><b>GID_ZOOM</b></td>
<td>3</td>
<td>The zoom gesture.</td>
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
 

<div class="alert"><b>Note</b>  
    The <b>GID_PAN</b> gesture has built-in inertia.  At the end of a pan gesture, additional pan
    gesture messages are created by the operating system.
    </div>
<div> </div>

The following type is defined to represent a constant pointer to a <b>GESTUREINFO</b> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    typedef GESTUREINFO const * PCGESTUREINFO;	 
</pre>
</td>
</tr>
</table></span></div>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&amp;gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &amp;gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr &gt; 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/407ed585-09aa-4174-8907-8bb9590f1795">GetGestureInfo</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>



<a href="https://msdn.microsoft.com/4167aeb0-2c31-4b7b-ad1b-e6d37da09ef8">WM_GESTURE</a>
 

 

