---
UID: NF:physicalmonitorenumerationapi.GetPhysicalMonitorsFromHMONITOR
title: GetPhysicalMonitorsFromHMONITOR function
author: windows-sdk-content
description: Retrieves the physical monitors associated with an HMONITOR monitor handle.
old-location: monitor\getphysicalmonitorsfromhmonitor.htm
tech.root: Monitor
ms.assetid: f2ac8a6a-3be9-4155-ad13-c256b96da792
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetPhysicalMonitorsFromHMONITOR, GetPhysicalMonitorsFromHMONITOR function [Monitor Configuration], monitor.getphysicalmonitorsfromhmonitor, physicalmonitorenumerationapi/GetPhysicalMonitorsFromHMONITOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: physicalmonitorenumerationapi.h
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
 - GetPhysicalMonitorsFromHMONITOR
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetPhysicalMonitorsFromHMONITOR function


## -description


Retrieves the physical monitors associated with an <b>HMONITOR</b> monitor handle.


## -parameters




### -param hMonitor [in]

A monitor handle. Monitor handles are returned by several Multiple Display Monitor functions, including <a href="https://msdn.microsoft.com/a7668c28-77c9-4373-ae1a-eab3cb98f866">EnumDisplayMonitors</a> and <a href="https://msdn.microsoft.com/fe6505c9-b481-4fec-ae9d-995943234a3a">MonitorFromWindow</a>, which are part of the graphics device interface (GDI).
          


### -param dwPhysicalMonitorArraySize [in]

Number of elements in <i>pPhysicalMonitorArray</i>. To get the required size of the array, call <a href="https://msdn.microsoft.com/c4cc3012-10ae-4435-8d81-e0a9eb62b55c">GetNumberOfPhysicalMonitorsFromHMONITOR</a>.
          


### -param pPhysicalMonitorArray [out]

Pointer to an array of <a href="https://msdn.microsoft.com/58eb4999-37d9-472d-aa26-38b19a2287b2">PHYSICAL_MONITOR</a> structures. The caller must allocate the array.
          


## -returns



If the function succeeds, the return value is <b>TRUE</b>. If the function fails, the return value is <b>FALSE</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.
          




## -remarks



A single <b>HMONITOR</b> handle can be associated with more than one physical monitor. This function returns a handle and a text description for each physical monitor.
      

When you are done using the monitor handles, close them by passing the <i>pPhysicalMonitorArray</i> array to the <a href="https://msdn.microsoft.com/ec9bbadf-93f3-4842-9bcc-e6a76f2f1ccf">DestroyPhysicalMonitors</a> function.
      


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HMONITOR hMonitor = NULL;
DWORD cPhysicalMonitors;
LPPHYSICAL_MONITOR pPhysicalMonitors = NULL;

// Get the monitor handle.
hMonitor = MonitorFromWindow(hWnd, MONITOR_DEFAULTTOPRIMARY);

// Get the number of physical monitors.
BOOL bSuccess = GetNumberOfPhysicalMonitorsFromHMONITOR(
  hMonitor, 
  &amp;cPhysicalMonitors
   );

if (bSuccess)
{
    // Allocate the array of PHYSICAL_MONITOR structures.
    pPhysicalMonitors = (LPPHYSICAL_MONITOR)malloc(
        cPhysicalMonitors* sizeof(PHYSICAL_MONITOR));

    if (pPhysicalMonitors != NULL)
    {
        // Get the array.
        bSuccess = GetPhysicalMonitorsFromHMONITOR(
            hMonitor, cPhysicalMonitors, pPhysicalMonitors);

       // Use the monitor handles (not shown).

        // Close the monitor handles.
        bSuccess = DestroyPhysicalMonitors(
            cPhysicalMonitors, 
            pPhysicalMonitors);

        // Free the array.
        free(pPhysicalMonitors);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e9a00792-f471-47a4-93d7-25400e27f13f">Monitor Configuration Functions</a>
 

 

