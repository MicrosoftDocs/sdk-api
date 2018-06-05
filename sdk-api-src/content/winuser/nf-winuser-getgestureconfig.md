---
UID: NF:winuser.GetGestureConfig
title: GetGestureConfig function
author: windows-sdk-content
description: Retrieves the configuration for which Windows Touch gesture messages are sent from a window.
old-location: wintouch\getgestureconfig.htm
old-project: wintouch
ms.assetid: 8b7a594c-e9e4-4215-8946-da170c957a2b
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetGestureConfig, GetGestureConfig function [Windows Touch], wintouch.getgestureconfig, winuser/GetGestureConfig
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
-	Ext-MS-Win-NTUser-Misc-l1-2-0.dll
-	Ext-MS-Win-NTUser-Misc-l1-3-0.dll
-	ext-ms-win-ntuser-misc-l1-3-1.dll
-	Ext-MS-Win-NTUser-Misc-L1-4-0.dll
-	Ext-Ms-Win-NTUser-Misc-L1-5-0.dll
-	Ext-MS-Win-NTUser-Misc-L1-5-1.dll
api_name:
-	GetGestureConfig
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

