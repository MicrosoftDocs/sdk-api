---
UID: NN:windows.devices.alljoyn.interop.IWindowsDevicesAllJoynBusAttachmentFactoryInterop
title: IWindowsDevicesAllJoynBusAttachmentFactoryInterop (windows.devices.alljoyn.interop.h)
description: This interface allows for the creation of alljoyn_busattachment without taking ownership of the reference.
helpviewer_keywords: ["IWindowsDevicesAllJoynBusAttachmentFactoryInterop","IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API]","IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API]","described","alljoyn.iwindowsdevicesalljoynbusattachmentfactoryinterop","windows/IWindowsDevicesAllJoynBusAttachmentFactoryInterop"]
old-location: alljoyn\iwindowsdevicesalljoynbusattachmentfactoryinterop.htm
tech.root: AllJoyn
ms.assetid: 2E9FE6B4-E8F0-4627-A712-F7A4CE5404BE
ms.date: 12/05/2018
ms.keywords: IWindowsDevicesAllJoynBusAttachmentFactoryInterop, IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API], IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface [AllJoyn API],described, alljoyn.iwindowsdevicesalljoynbusattachmentfactoryinterop, windows/IWindowsDevicesAllJoynBusAttachmentFactoryInterop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWindowsDevicesAllJoynBusAttachmentFactoryInterop
 - windows.devices.alljoyn.interop/IWindowsDevicesAllJoynBusAttachmentFactoryInterop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.devices.alljoyn.interop.h
api_name:
 - IWindowsDevicesAllJoynBusAttachmentFactoryInterop
---

# IWindowsDevicesAllJoynBusAttachmentFactoryInterop interface


## -description

This interface allows for the creation of <b>alljoyn_busattachment</b> without taking ownership of the reference.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWindowsDevicesAllJoynBusAttachmentFactoryInterop</b> interface inherits from <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>. <b>IWindowsDevicesAllJoynBusAttachmentFactoryInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWindowsDevicesAllJoynBusAttachmentFactoryInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/windows.devices.alljoyn.interop/nf-windows-devices-alljoyn-interop-iwindowsdevicesalljoynbusattachmentfactoryinterop-createfromwin32handle">CreateFromWin32Handle</a>
</td>
<td align="left" width="63%">
Constructs an <b>AllJoynBusAttachment</b> over an existing <b>alljoyn_busattachment</b> instance without taking ownership.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable </a>