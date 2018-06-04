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

# DPI_AWARENESS enumeration


## -description


Identifies the dots per inch (dpi) setting for a thread, process, or window.


## -enum-fields




### -field DPI_AWARENESS_INVALID

Invalid DPI awareness. This is an invalid DPI awareness value.


### -field DPI_AWARENESS_UNAWARE

DPI unaware. This process does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI). It will be automatically scaled by the system on any other DPI setting.


### -field DPI_AWARENESS_SYSTEM_AWARE

System DPI aware. This process does not scale for DPI changes. It will query for the DPI once and use that value for the lifetime of the process. If the DPI changes, the process will not adjust to the new DPI value. It will be automatically scaled up or down by the system when the DPI changes from the system value.


### -field DPI_AWARENESS_PER_MONITOR_AWARE

Per monitor DPI aware. This process checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes. These processes are not automatically scaled by the system.


## -remarks



In previous versions of Windows, DPI values were only set once for an entire application. For those apps, the <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a> type determined the type of DPI awareness for the entire application. Currently, the DPI awareness is defined on an individual thread, window, or process level and is indicated by the <b>DPI_AWARENESS</b> type. While the focus shifted from a process level to a thread level, the different kinds of DPI awareness are the same: unaware, system aware, and per monitor aware. For detailed descriptions and some examples of the different DPI kinds, see <b>PROCESS_DPI_AWARENESS</b>.

The old recommendation was to define the DPI awareness level in the application manifest using the setting <i>dpiAware</i> as explained in <a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>. Now that the DPI awareness is tied to threads and windows instead of an entire application, a new windows setting is added to the app manifest. This setting is <i>dpiAwareness</i> and will override any <i>dpiAware</i> setting if both of them are present in the manifest. While it is still recommended to use the manifest, you can now change the DPI awareness while the app is running by using <a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>.

It is important to note that if your application has a <b>DPI_AWARENESS_PER_MONITOR_AWARE</b> window, you are responsible for keeping track of the DPI by responding to <a href="https://msdn.microsoft.com/97C458F2-89CD-45FF-ABEE-F158A3BCE0B8">WM_DPICHANGED</a> messages.


#### Examples

This snippet demonstrates how to set a value of <b>DPI_AWARENESS_SYSTEM_AWARE</b> in your application manifest.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;dpiAwareness&gt;System&lt;/dpiAwareness&gt;</pre>
</td>
</tr>
</table></span></div>
This snippet demonstrates how to set a value of <b>DPI_AWARENESS_PER_MONITOR_AWARE</b> in your application manifest.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;dpiAwareness&gt;PerMonitor&lt;/dpiAwareness&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/50130739-E8A8-4B92-9B80-3BBBE57EBE0C">PROCESS_DPI_AWARENESS</a>



<a href="https://msdn.microsoft.com/95531BDC-3D45-4BB6-8C63-0D845C66B88F">SetThreadDpiAwarenessContext</a>
 

 

