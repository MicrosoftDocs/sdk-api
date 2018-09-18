---
UID: NF:lowlevelmonitorconfigurationapi.CapabilitiesRequestAndCapabilitiesReply
title: CapabilitiesRequestAndCapabilitiesReply function
author: windows-sdk-content
description: Retrieves a string describing a monitor's capabilities.
old-location: monitor\capabilitiesrequestandcapabilitiesreply.htm
tech.root: Monitor
ms.assetid: 1e556f66-a77a-43f3-b54f-d14995d841f8
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CapabilitiesRequestAndCapabilitiesReply, CapabilitiesRequestAndCapabilitiesReply function [Monitor Configuration], lowlevelmonitorconfigurationapi/CapabilitiesRequestAndCapabilitiesReply, monitor.capabilitiesrequestandcapabilitiesreply
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxva2.dll
api_name:
 - CapabilitiesRequestAndCapabilitiesReply
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CapabilitiesRequestAndCapabilitiesReply function


## -description


Retrieves a string describing a monitor's capabilities.


## -parameters




### -param hMonitor [in]

Handle to a physical monitor. To get the monitor handle, call <a href="https://msdn.microsoft.com/f2ac8a6a-3be9-4155-ad13-c256b96da792">GetPhysicalMonitorsFromHMONITOR</a> or <a href="https://msdn.microsoft.com/1e0e9749-8ee4-42d5-ab7b-182222b6c429">GetPhysicalMonitorsFromIDirect3DDevice9</a>.
          


### -param pszASCIICapabilitiesString [out]

Pointer to a buffer that receives the monitor's capabilities string. The caller must allocate this buffer. To get the size of the string, call <a href="https://msdn.microsoft.com/fe38e63d-b5b8-4b64-b7cb-9ff1c20a2e4a">GetCapabilitiesStringLength</a>. The capabilities string is always an ASCII string. The buffer must include space for the terminating null character.
          


### -param dwCapabilitiesStringLengthInCharacters [in]

Size of <i>pszASCIICapabilitiesString</i> in characters, including the terminating null character.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



This function corresponds to the "Capabilities Request &amp; Capabilities Reply" command from the Display Data Channel Command Interface (DDC/CI) standard. For more information about the capabilities string, refer to the DDC/CI standard.
      

This function usually returns quickly, but sometimes it can take several seconds to complete.
      

You can update a monitor's capabilities string by adding an <i>AddReg</i> directive to the monitor's INF file. Add a registry key named "CapabilitiesString" to the monitor's driver key. The value of the registry key is the capabilities string. The registry data type is REG_SZ.

<pre class="syntax" xml:space="preserve"><code>HKR,,"CapabilitiesString",0x00000000,"updated capabilities string"
</code></pre>
<div class="alert"><b>Warning</b>  Do not modify a monitor's INF file unless you are familiar with the layout of INF files and also understand the DDC/CI standard.</div>
<div> </div>

#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
DWORD cchStringLength = 0;
BOOL bSuccess = 0;
LPSTR szCapabilitiesString = NULL;

// Get the length of the string.
bSuccess = GetCapabilitiesStringLength(
   hPhysicalMonitor, // Handle to the monitor.
   &amp;cchStringLength
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
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

