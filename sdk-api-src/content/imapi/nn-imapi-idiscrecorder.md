---
UID: NN:imapi.IDiscRecorder
title: IDiscRecorder (imapi.h)
author: windows-sdk-content
description: The IDiscRecorder interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as MSDiscMasterObj maintains an active disc recorder.
old-location: imapi\idiscrecorder.htm
tech.root: imapi
ms.assetid: fc861cbb-a14e-499e-8b80-f5912e4f6076
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscRecorder, IDiscRecorder interface [IMAPI], IDiscRecorder interface [IMAPI],described, _win32_idiscrecorder, base.idiscrecorder, imapi.idiscrecorder, imapi/IDiscRecorder
ms.topic: interface
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscRecorder
 - IDiscRecorder.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder interface


## -description


The 
<b>IDiscRecorder</b> interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as <b>MSDiscMasterObj</b> maintains an active disc recorder.

An 
<b>IDiscRecorder</b> object represents a single hardware device, but there can be multiple instances of 
<b>IDiscRecorder</b> all referencing the same hardware device. In this case, use 
<a href="https://msdn.microsoft.com/e704baf0-d403-4cf7-aa32-16677d9a8694">OpenExclusive</a> to access that device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDiscRecorder</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDiscRecorder</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39af9413-6068-4165-8a26-509389a6d1f2">Close</a>
</td>
<td align="left" width="63%">
Closes a recorder after exclusive access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29a40f49-1567-4198-b682-a0e314858baf">Eject</a>
</td>
<td align="left" width="63%">
Ejects a recorder's tray, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61a9cada-a9f4-462d-ab73-a9319308ff01">Erase</a>
</td>
<td align="left" width="63%">
Erases CD-RW media, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02ca36dd-bd76-41b8-90ce-6c026152cdbe">GetBasePnPID</a>
</td>
<td align="left" width="63%">
Retrieves identifier unique to device class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0f20cae4-3f9c-49bb-9b82-13351b889a31">GetDisplayNames</a>
</td>
<td align="left" width="63%">
Retrieves a name suitable for GUI display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bceb7302-e5e6-4ee5-9adb-1736ab62e819">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves a path to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d13d352-bc48-43c7-9800-12855d754435">GetRecorderGUID</a>
</td>
<td align="left" width="63%">
Retrieves the underlying device GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24d46cbc-56fd-4c9f-933c-0207dea5ada5">GetRecorderProperties</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface for the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7fa57f8b-33c4-475c-958c-1e2c4973e23a">GetRecorderState</a>
</td>
<td align="left" width="63%">
Checks if recorder is ready to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/287516b5-5d27-4277-8bc4-e2409b2a8cd7">GetRecorderType</a>
</td>
<td align="left" width="63%">
Identifies a device as CD-R or CD-RW.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%"><b>Init</b></td>
<td align="left" width="63%">
Initializes the object for an underlying device. 




Used internally only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e704baf0-d403-4cf7-aa32-16677d9a8694">OpenExclusive</a>
</td>
<td align="left" width="63%">
Opens a device for exclusive use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e97d5e5-1a10-4ef2-b083-427d4070283f">QueryMediaInfo</a>
</td>
<td align="left" width="63%">
Retrieves media properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40f9376d-5702-4dfb-a69b-0ca4fcfc8d8e">QueryMediaType</a>
</td>
<td align="left" width="63%">
Identifies the type of media in the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8da0add7-6a9d-46f4-b34c-7ea9aa0b7d3a">SetRecorderProperties</a>
</td>
<td align="left" width="63%">
Sets properties for the recorder.

</td>
</tr>
</table> 


## -remarks



All 
<b>IDiscRecorder</b> interfaces may be used on an 
<b>IDiscRecorder</b> object even if the disc recorder is not the active disc recorder. The IMAPI client does not have to call 
<a href="https://msdn.microsoft.com/5f2e9135-d251-4702-b5d1-51d9b445a4f5">IDiscMaster::SetActiveDiscRecorder</a> first.



