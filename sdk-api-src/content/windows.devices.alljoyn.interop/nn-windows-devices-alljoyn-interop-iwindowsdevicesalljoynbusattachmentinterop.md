---
UID: NN:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentInterop
title: IWindowsDevicesAllJoynBusAttachmentInterop
author: windows-sdk-content
description: This interface allows for retrieval of the underlying alljoyn_busattachment object.
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentinterop.htm
tech.root: AllJoyn
ms.assetid: F08A2D95-A84E-47C9-9485-98306993DB52
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWindowsDevicesAllJoynBusAttachmentInterop, IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API], IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API],described, alljoyn.iwindowsdevicesalljoynbusattachmentinterop, windows/IWindowsDevicesAllJoynBusAttachmentInterop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: windows.devices.alljoyn.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.devices.alljoyn.interop.h
api_name:
 - IWindowsDevicesAllJoynBusAttachmentInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWindowsDevicesAllJoynBusAttachmentInterop interface


## -description


This interface allows for retrieval of the underlying <b>alljoyn_busattachment</b> object.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDevicesAllJoynBusAttachmentInterop</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>. <b>IWindowsDevicesAllJoynBusAttachmentInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsDevicesAllJoynBusAttachmentInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E46C47FC-08D2-4CE6-9205-46A840DFA3F4">get_Win32Handle</a>
</td>
<td align="left" width="63%">
Classic COM interface that simply returns a pointer to the underlying <b>alljoyn_busattachment</b> instance, so the app can use it directly with the AllJoyn Core C API.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>
 

 

