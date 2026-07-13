---
UID: NF:sysinfoapi.GetIntegratedDisplaySize
title: GetIntegratedDisplaySize function (sysinfoapi.h)
description: Retrieves the best estimate of the diagonal size of the built-in screen, in inches.
helpviewer_keywords: ["GetIntegratedDisplaySize","GetIntegratedDisplaySize function","base.getintegrateddisplaysize","sysinfoapi/GetIntegratedDisplaySize"]
old-location: base\getintegrateddisplaysize.htm
tech.root: winprog
ms.assetid: EA155FCF-3245-498B-BEC8-742DE38DE258
ms.date: 12/05/2018
ms.keywords: GetIntegratedDisplaySize, GetIntegratedDisplaySize function, base.getintegrateddisplaysize, sysinfoapi/GetIntegratedDisplaySize
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
req.lib: onecore.lib
req.dll: kernelbase.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetIntegratedDisplaySize
 - sysinfoapi/GetIntegratedDisplaySize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - API-MS-Win-Core-SysInfo-L1-2-3.dll
 - KernelBase.dll
api_name:
 - GetIntegratedDisplaySize
---

# GetIntegratedDisplaySize function


## -description



Retrieves the best estimate of the diagonal size of the built-in screen, in inches.

## -parameters

### -param sizeInInches [out]

The best estimate of the diagonal size of the built-in screen, in inches.

## -returns

The result code indicating if the function succeeded or failed.

## -remarks

Uses the display driver as the source for display size information. Registry overrides to screen size will not be used. Uses the display adapter connection type to determine which display, if any, is integral to the system.  If no internal display detected, an error will be returned.   This requires the display to be active to be detected. For example, the lid cannot be closed when the function is called.

To compile an application that uses this function, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

The following function displays the best estimate of the diagonal size of the built-in screen, in inches.


```cpp
void ShowIntegratedDisplaySize()
{
  Platform::String^ buffer;
   
  double sizeInInches;
  HRESULT result = GetIntegratedDisplaySize(&sizeInInches) ;

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

```

## -see-also

<a href="/windows/desktop/SysInfo/system-information-functions">System
		  Information Functions</a>