---
UID: NF:lowlevelmonitorconfigurationapi.CapabilitiesRequestAndCapabilitiesReply
title: CapabilitiesRequestAndCapabilitiesReply function (lowlevelmonitorconfigurationapi.h)
description: Retrieves a string describing a monitor's capabilities.
helpviewer_keywords: ["CapabilitiesRequestAndCapabilitiesReply","CapabilitiesRequestAndCapabilitiesReply function [Monitor Configuration]","lowlevelmonitorconfigurationapi/CapabilitiesRequestAndCapabilitiesReply","monitor.capabilitiesrequestandcapabilitiesreply"]
old-location: monitor\capabilitiesrequestandcapabilitiesreply.htm
tech.root: Monitor
ms.assetid: 1e556f66-a77a-43f3-b54f-d14995d841f8
ms.date: 12/05/2018
ms.keywords: CapabilitiesRequestAndCapabilitiesReply, CapabilitiesRequestAndCapabilitiesReply function [Monitor Configuration], lowlevelmonitorconfigurationapi/CapabilitiesRequestAndCapabilitiesReply, monitor.capabilitiesrequestandcapabilitiesreply
req.header: lowlevelmonitorconfigurationapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxva2.lib
req.dll: Dxva2.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CapabilitiesRequestAndCapabilitiesReply
 - lowlevelmonitorconfigurationapi/CapabilitiesRequestAndCapabilitiesReply
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - CapabilitiesRequestAndCapabilitiesReply
---

# CapabilitiesRequestAndCapabilitiesReply function

## -description

> [!WARNING]
> The physical monitor configuration functions work using the VESA Monitor Control Command Set (MCCS) standard over an I<sup>2</sup>C interface. Many monitors don't fully implement that standard; so your use of these commands might result in undefined monitor behavior. We don't recommend using these functions for arbitrary monitors without physically validating that they work as intended.

Retrieves a string describing a monitor's capabilities.

## -parameters

### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor">GetPhysicalMonitorsFromHMONITOR</a> or <a href="/windows/desktop/api/physicalmonitorenumerationapi/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9">GetPhysicalMonitorsFromIDirect3DDevice9</a>.

### -param pszASCIICapabilitiesString [out]

Pointer to a buffer that receives the monitor's capabilities string. The caller must allocate this buffer. To get the size of the string, call <a href="/windows/desktop/api/lowlevelmonitorconfigurationapi/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength">GetCapabilitiesStringLength</a>. The capabilities string is always an ASCII string. The buffer must include space for the terminating null character.

### -param dwCapabilitiesStringLengthInCharacters [in]

Size of <i>pszASCIICapabilitiesString</i> in characters, including the terminating null character.

## -returns

If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

This function corresponds to the "Capabilities Request &amp; Capabilities Reply" command from the Display Data Channel Command Interface (DDC/CI) standard. For more information about the capabilities string, refer to the DDC/CI standard.
      

This function usually returns quickly, but sometimes it can take several seconds to complete.
      

You can update a monitor's capabilities string by adding an <i>AddReg</i> directive to the monitor's INF file. Add a registry key named "CapabilitiesString" to the monitor's driver key. The value of the registry key is the capabilities string. The registry data type is REG_SZ.


``` syntax
HKR,,"CapabilitiesString",0x00000000,"updated capabilities string"

```

<div class="alert"><b>Warning</b>  Do not modify a monitor's INF file unless you are familiar with the layout of INF files and also understand the DDC/CI standard.</div>
<div> </div>

#### Examples


```cpp

DWORD cchStringLength = 0;
BOOL bSuccess = 0;
LPSTR szCapabilitiesString = NULL;

// Get the length of the string.
bSuccess = GetCapabilitiesStringLength(
   hPhysicalMonitor, // Handle to the monitor.
   &cchStringLength
   );

if (bSuccess)
{
    // Allocate the string buffer.
    LPSTR szCapabilitiesString = (LPSTR)malloc(cchStringLength);
    if (szCapabilitiesString != NULL)
    {
        // Get the capabilities string.
        bSuccess = CapabilitiesRequestAndCapabilitiesReply(
            hPhysicalMonitor,
            szCapabilitiesString,
            cchStringLength
            );

        // Free the string buffer.
        free(szCapabilitiesString);
    }
}

```

## -see-also

<a href="/windows/desktop/Monitor/monitor-configuration-functions">Monitor Configuration Functions</a>
