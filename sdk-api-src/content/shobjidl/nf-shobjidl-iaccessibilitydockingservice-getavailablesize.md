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

# IAccessibilityDockingService::GetAvailableSize


## -description


Retrieves the dimensions available on a specific screen for displaying an accessibility window.


## -parameters




### -param hMonitor [in]

Type: <b>HMONITOR</b>

The handle of the monitor whose available docking size is to be retrieved. For information on how to retrieve an <b>HMONITOR</b>, see <a href="https://msdn.microsoft.com/fe6505c9-b481-4fec-ae9d-995943234a3a">MonitorFromWindow</a>.


### -param pcxFixed [out]

Type: <b>UINT*</b>

When this method returns successfully, this parameter receives the fixed width, in physical pixels, available for docking on the specified monitor. Any window docked to this monitor will be sized to this width.

                        

If the method fails, this value is set to 0.

If this value is <b>NULL</b>, an access violation will occur.


### -param pcyMax [out]

Type: <b>UINT*</b>

When this method returns successfully, this parameter receives the maximum height, in physical pixels, available for a docked window on the specified monitor.

                        

If the method fails, this value is set to 0.

If this value is <b>NULL</b>, an access violation will occur.


## -returns



Type: <b>HRESULT</b>

Returns a standard return value, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_MONITOR_HANDLE)</b></dt>
</dl>
</td>
<td width="60%">
The monitor specified by <i>hMonitor</i> does not support docking.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="When_to_use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to use</h3>
A docked accessibility window is limited in the amount of space that it can use on any screen. Therefore, before trying to dock an accessibility window, call this function to get the available dimensions. You cannot dock any window that would cause a Windows Store app to have access to less than 768 vertical screen pixels.


#### Examples

This example shows this method in use.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
 IAccessibilityDockingService *pDockingService;
 
 HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&amp;pDockingService));
 if (SUCCEEDED(hr)) 
 {
     UINT uMaxHeight;
     UINT uFixedWidth;

     HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
     if (hMonitor != nullptr)
     {
         hr = pDockingService-&gt;GetAvailableSize(hMonitor, &amp;uMaxHeight, &amp;uFixedWidth);
     }
 }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/EB66604E-4665-4d62-878C-7777C1C042F3">IAccessibilityDockingService</a>
 

 

