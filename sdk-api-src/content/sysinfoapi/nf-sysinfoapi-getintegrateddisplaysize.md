---
UID: NF:sysinfoapi.GetIntegratedDisplaySize
title: GetIntegratedDisplaySize function
author: windows-sdk-content
description: Retrieves the best estimate of the diagonal size of the built-in screen, in inches.
old-location: base\getintegrateddisplaysize.htm
tech.root: sysinfo
ms.assetid: EA155FCF-3245-498B-BEC8-742DE38DE258
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: GetIntegratedDisplaySize, GetIntegratedDisplaySize function, base.getintegrateddisplaysize, sysinfoapi/GetIntegratedDisplaySize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sysinfoapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-SysInfo-L1-2-3.dll
 - KernelBase.dll
api_name:
 - GetIntegratedDisplaySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIntegratedDisplaySize function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Retrieves the best estimate of the diagonal size of the built-in screen, in inches.


## -parameters




### -param sizeInInches [out]

The best estimate of the diagonal size of the built-in screen, in inches.


## -returns



The result code indicating if the function succeeded or failed.




## -remarks



Uses the display driver as the source for display size information. Registry overrides to screen size will not be used. Uses the display adapter connection type to determine which display, if any, is integral to the system.  If no internal display detected, an error will be returned.   This requires the display to be active to be detected. For example, the lid cannot be closed when the function is called.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.


#### Examples

The following function displays the best estimate of the diagonal size of the built-in screen, in inches.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void ShowIntegratedDisplaySize()
{
  Platform::String^ buffer;
   
  double sizeInInches;
  HRESULT result = GetIntegratedDisplaySize(&amp;sizeInInches) ;

  if (SUCCEEDED(result))
  {
    buffer += "Internal display size is " + sizeInInches.ToString() + " inches.\n"; 
  }
  else 
  {
    buffer += "No valid Internal display found. \n";
  }

  // Output the string buffer here... 
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/aa7deebf-7dce-4147-8a15-1d7411aea0fa">System
		  Information Functions</a>
 

 

