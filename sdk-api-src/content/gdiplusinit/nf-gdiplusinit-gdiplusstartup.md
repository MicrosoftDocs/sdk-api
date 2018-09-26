---
UID: NF:gdiplusinit.GdiplusStartup
title: GdiplusStartup function
author: windows-sdk-content
description: The GdiplusStartup function initializes Windows GDI+. Call GdiplusStartup before making any other GDI+ calls, and call GdiplusShutdown when you have finished using GDI+.
old-location: gdiplus\_gdiplus_FUNC_GdiplusStartup_token_input_output_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\gdiplusstartup.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GdiplusStartup, GdiplusStartup function [GDI+], _gdiplus_FUNC_GdiplusStartup_token_input_output_, gdiplus._gdiplus_FUNC_GdiplusStartup_token_input_output_, gdiplusinit/GdiplusStartup
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gdiplusinit.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gdiplus.dll
api_name:
 - GdiplusStartup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GdiplusStartup function


## -description


The <b>GdiplusStartup</b> function initializes Windows GDI+. Call <b>GdiplusStartup</b> before making any other GDI+ calls, and call <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> when you have finished using GDI+.


## -parameters




### -param token [out]

Type: <b>ULONG_PTR token*</b>

Pointer to a 
					<b>ULONG_PTR</b> that receives a token. Pass the token to <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> when you have finished using GDI+. 


### -param input [in]

Type: <b>const <a href="https://msdn.microsoft.com/en-us/library/ms534067(v=VS.85).aspx">GdiplusStartupInput</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534067(v=VS.85).aspx">GdiplusStartupInput</a> structure that contains the GDI+ version, a pointer to a debug callback function, a Boolean value that specifies whether to suppress the background thread, and a Boolean value that specifies whether to suppress external image codecs. 


### -param output [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534068(v=VS.85).aspx">GdiplusStartupOutput</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534068(v=VS.85).aspx">GdiplusStartupOutput</a> structure that receives a pointer to a notification hook function and a pointer to a notification unhook function. If the 
					<b>SuppressBackgroundThread</b> data member of the 
					<i>input</i> parameter is <b>FALSE</b>, then this parameter can be <b>NULL</b>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the function succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the function fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -remarks



You must call <b>GdiplusStartup</b> before you create any GDI+ objects, and you must delete all of your GDI+ objects (or have them go out of scope) before you call <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a>.

You can call <b>GdiplusStartup</b> on one thread and call <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> on another thread as long as you delete all of your GDI+ objects (or have them go out of scope) before you call <b>GdiplusShutdown</b>.

Do not call <b>GdiplusStartup</b> or <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> in 
				<a href="https://msdn.microsoft.com/0c3e3083-9297-4626-b2a7-0062d1c2cf9e">DllMain</a> or in any function that is called by DllMain. If you want to create a DLL that uses GDI+, you should use one of the following techniques to initialize GDI+:

<ul>
<li>Require your clients to call <b>GdiplusStartup</b> before they call the functions in your DLL and to call <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> when they have finished using your DLL. </li>
<li>Export your own startup function that calls <b>GdiplusStartup</b> and your own shutdown function that calls <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a>. Require your clients to call your startup function before they call other functions in your DLL and to call your shutdown function when they have finished using your DLL. </li>
<li>Call <b>GdiplusStartup</b> and <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> in each of your functions that make GDI+ calls. </li>
</ul>
<div class="alert"><b>Warning</b>  For info about how to use dynamic data exchange (DDE) with GDI+, see <a href="http://go.microsoft.com/fwlink/p/?linkid=237639">Special CWinApp Services</a>.</div>
<div> </div>

#### Examples



For an example of calling <b>GdiplusStartup</b> and <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> in a Windows application, see <a href="https://msdn.microsoft.com/en-us/library/ms533807(v=VS.85).aspx">Getting Started</a>.

The following console application uses a GDI+<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a> object to retrieve the width and height of a JPEG image. The code calls <b>GdiplusStartup</b> before creating the 
						<b>Image</b> object and calls <a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a> before terminating. Note that the 
						<b>Image</b> object is deleted before the call to <b>GdiplusShutdown</b>.

In the following code, the variable 
						<i>gdiplusStartupInput</i> is initialized by the default constructor of the <a href="https://msdn.microsoft.com/en-us/library/ms534067(v=VS.85).aspx">GdiplusStartupInput</a> structure. The default constructor sets the data members of the structure to the following values: 

<ul>
<li><b>GdiplusVersion</b> = 1 </li>
<li><b>DebugEventCallback</b> = <b>NULL</b></li>
<li><b>SuppressBackgroundThread</b> = <b>FALSE</b></li>
<li><b>SuppressExternalCodecs</b> = <b>FALSE</b></li>
</ul>

```cpp
#include <windows.h>
#include <gdiplus.h>
#include <stdio.h>
using namespace Gdiplus;

INT main()
{
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR gdiplusToken;
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);

   Image* image = new Image(L"FakePhoto.jpg");
   printf("The width of the image is %u.\n", image->GetWidth());
   printf("The height of the image is %u.\n", image->GetHeight()); 

   delete image;
   GdiplusShutdown(gdiplusToken);
   return 0;
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534076(v=VS.85).aspx">GdiplusShutdown</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534067(v=VS.85).aspx">GdiplusStartupInput</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534068(v=VS.85).aspx">GdiplusStartupOutput</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533807(v=VS.85).aspx">Getting Started</a>
 

 

