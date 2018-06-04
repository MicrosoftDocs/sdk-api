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

# GetGestureConfig function


## -description



  Retrieves the configuration for which Windows  Touch gesture messages are sent from a window.
  


## -parameters




### -param hwnd [in]

A handle to the window to get the gesture configuration from.


### -param dwReserved [in]

This value is reserved and must be set to 0.


### -param dwFlags [in]

A gesture command flag value indicating options for retrieving the gesture configuration.  See Remarks for additional information and supported values.


### -param pcIDs [in]

The size, in number of gesture configuration structures, that is in the <i>pGestureConfig</i> buffer.


### -param pGestureConfig [in, out]

An array of gesture configuration structures that specify the gesture configuration.


### -param cbSize [in]

The size of the gesture configuration (<a href="https://msdn.microsoft.com/4ec5050e-7fef-4f52-89af-5237e8cdbdb8">GESTURECONFIG</a>) structure.


## -returns



If the function succeeds, the return value is nonzero.
     



If the function fails, the return value is zero. To get extended error information, use the <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> function.




## -remarks




      Passing a value other than <code>sizeof(GESTURECONFIG)</code> for the 
      <i>cbSize</i> parameter will cause calls to this function to fail and 
      <a href="http://msdn.microsoft.com/en-us/library/ms679360.aspx">GetLastError</a> will 
      return <b>ERROR_INVALID_PARAMETER</b> (87 in decimal).    
      


  The following table lists the gesture configuration values:
  

<table>
<tr>
<th>Name</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>GCF_INCLUDE_ANCESTORS</b></td>
<td>0x00000001</td>
<td>If specified, <b>GetGestureConfig</b> returns consolidated configuration for the specified window and its parent window chain.</td>
</tr>
</table>
 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    GESTURECONFIG gc[3];    
    UINT uiGcs = 3;

    ZeroMemory(&amp;gc, sizeof(gc));
    gc[0].dwID  = GID_ZOOM;
    gc[1].dwID  = GID_ROTATE;
    gc[2].dwID  = GID_PAN;
    BOOL bResult = GetGestureConfig(hWnd, 0, 0, &amp;uiGcs, gc, sizeof(GESTURECONFIG));        
    if (!bResult){                
        DWORD err = GetLastError();                                       
    }    
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>



<a href="https://msdn.microsoft.com/4ec5050e-7fef-4f52-89af-5237e8cdbdb8">GESTURECONFIG</a>



<a href="https://msdn.microsoft.com/afd61b18-4e54-44c5-9b71-74908c76c7ac">Programming Guide for Gestures</a>
 

 

