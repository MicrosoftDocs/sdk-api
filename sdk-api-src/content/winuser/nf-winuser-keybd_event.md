---
UID: NF:winuser.keybd_event
title: keybd_event function
author: windows-sdk-content
description: Synthesizes a keystroke.
old-location: inputdev\keybd_event.htm
old-project: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\keyboardinput\keyboardinputreference\keyboardinputfunctions\keybd_event.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: KEYEVENTF_EXTENDEDKEY, KEYEVENTF_KEYUP, _win32_keybd_event, _win32_keybd_event_cpp, inputdev.keybd_event, keybd_event, keybd_event function [Keyboard and Mouse Input], winui._win32_keybd_event, winuser/keybd_event
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - keybd_event
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# keybd_event function


## -description


Synthesizes a keystroke. The system can use such a synthesized keystroke to generate a <a href="https://msdn.microsoft.com/en-us/library/ms646281(v=VS.85).aspx">WM_KEYUP</a> or <a href="https://msdn.microsoft.com/en-us/library/ms646280(v=VS.85).aspx">WM_KEYDOWN</a> message. The keyboard driver's interrupt handler calls the <b>keybd_event</b> function.
<div class="alert"><b>Note</b>  This function has been superseded. Use <a href="https://msdn.microsoft.com/en-us/library/ms646310(v=VS.85).aspx">SendInput</a> instead.</div><div> </div>

## -parameters




### -param bVk [in]

Type: <b>BYTE</b>

A virtual-key code. The code must be a value in the range 1 to 254. For a complete list, see <a href="https://msdn.microsoft.com/en-us/library/Dd375731(v=VS.85).aspx">Virtual Key Codes</a>. 


### -param bScan [in]

Type: <b>BYTE</b>

A hardware scan code for the key.


### -param dwFlags [in]

Type: <b>DWORD</b>

Controls various aspects of function operation. This parameter can be one or more of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_EXTENDEDKEY"></a><a id="keyeventf_extendedkey"></a><dl>
<dt><b>KEYEVENTF_EXTENDEDKEY</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
If specified, the scan code was preceded by a prefix byte having the value 0xE0 (224).

</td>
</tr>
<tr>
<td width="40%"><a id="KEYEVENTF_KEYUP"></a><a id="keyeventf_keyup"></a><dl>
<dt><b>KEYEVENTF_KEYUP</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
If specified, the key is being released. If not specified, the key is being depressed.

</td>
</tr>
</table>
 


### -param dwExtraInfo [in]

Type: <b>ULONG_PTR</b>

An additional value associated with the key stroke. 


## -returns



This function does not return a value.




## -remarks



An application can simulate a press of the PRINTSCRN key in order to obtain a screen snapshot and save it to the clipboard. To do this, call <b>keybd_event</b> with the 
				<i>bVk</i> parameter set to <b>VK_SNAPSHOT</b>. 


#### Examples

The following sample program toggles the NUM LOCK light by using <b>keybd_event</b> with a virtual key of <b>VK_NUMLOCK</b>. It takes a Boolean value that indicates whether the light should be turned off (<b>FALSE</b>) or on (<b>TRUE</b>). The same technique can be used for the CAPS LOCK key (<b>VK_CAPITAL</b>) and the SCROLL LOCK key (<b>VK_SCROLL</b>).

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
   #include &lt;windows.h&gt;

   void SetNumLock( BOOL bState )
   {
      BYTE keyState[256];

      GetKeyboardState((LPBYTE)&amp;keyState);
      if( (bState &amp;&amp; !(keyState[VK_NUMLOCK] &amp; 1)) ||
          (!bState &amp;&amp; (keyState[VK_NUMLOCK] &amp; 1)) )
      {
      // Simulate a key press
         keybd_event( VK_NUMLOCK,
                      0x45,
                      KEYEVENTF_EXTENDEDKEY | 0,
                      0 );

      // Simulate a key release
         keybd_event( VK_NUMLOCK,
                      0x45,
                      KEYEVENTF_EXTENDEDKEY | KEYEVENTF_KEYUP,
                      0);
      }
   }

   void main()
   {
      SetNumLock( TRUE );
   }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646293(v=VS.85).aspx">GetAsyncKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646301(v=VS.85).aspx">GetKeyState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645530(v=VS.85).aspx">Keyboard Input</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646306(v=VS.85).aspx">MapVirtualKey</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646314(v=VS.85).aspx">SetKeyboardState</a>



<a href="https://msdn.microsoft.com/en-us/library/ms646304(v=VS.85).aspx">keybd_event</a>
 

 

