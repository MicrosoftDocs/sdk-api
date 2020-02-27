---
UID: NN:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentInterop
title: IWindowsDevicesAllJoynBusAttachmentInterop (windows.devices.alljoyn.interop.h)
description: This interface allows for retrieval of the underlying alljoyn_busattachment object.
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentinterop.htm
tech.root: AllJoyn
ms.assetid: F08A2D95-A84E-47C9-9485-98306993DB52
ms.date: 12/05/2018
ms.keywords: IWindowsDevicesAllJoynBusAttachmentInterop, IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API], IWindowsDevicesAllJoynBusAttachmentInterop interface [AllJoyn API],described, alljoyn.iwindowsdevicesalljoynbusattachmentinterop, windows/IWindowsDevicesAllJoynBusAttachmentInterop
f1_keywords:
- windows.devices.alljoyn.interop/IWindowsDevicesAllJoynBusAttachmentInterop
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWindowsDevicesAllJoynBusAttachmentInterop interface


## -description


This interface allows for retrieval of the underlying <b>alljoyn_busattachment</b> object.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDevicesAllJoynBusAttachmentInterop</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>. <b>IWindowsDevicesAllJoynBusAttachmentInterop</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.devices.alljoyn.interop/nf-windows-devices-alljoyn-interop-iwindowsdevicesalljoynbusattachmentinterop-get_win32handle">get_Win32Handle</a>
</td>
<td align="left" width="63%">
Classic COM interface that simply returns a pointer to the underlying <b>alljoyn_busattachment</b> instance, so the app can use it directly with the AllJoyn Core C API.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>
 

 

