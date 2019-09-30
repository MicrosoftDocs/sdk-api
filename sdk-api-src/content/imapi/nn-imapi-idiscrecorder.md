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
f1_keywords: 
 - "imapi/IDiscRecorder"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscRecorder interface


## -description


The 
<b>IDiscRecorder</b> interface enables access to a single disc recorder device, labeled the active disc recorder. An IMAPI object such as <b>MSDiscMasterObj</b> maintains an active disc recorder.

An 
<b>IDiscRecorder</b> object represents a single hardware device, but there can be multiple instances of 
<b>IDiscRecorder</b> all referencing the same hardware device. In this case, use 
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-openexclusive">OpenExclusive</a> to access that device.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDiscRecorder</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDiscRecorder</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-close">Close</a>
</td>
<td align="left" width="63%">
Closes a recorder after exclusive access.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-eject">Eject</a>
</td>
<td align="left" width="63%">
Ejects a recorder's tray, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-erase">Erase</a>
</td>
<td align="left" width="63%">
Erases CD-RW media, if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getbasepnpid">GetBasePnPID</a>
</td>
<td align="left" width="63%">
Retrieves identifier unique to device class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getdisplaynames">GetDisplayNames</a>
</td>
<td align="left" width="63%">
Retrieves a name suitable for GUI display.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getpath">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves a path to the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecorderguid">GetRecorderGUID</a>
</td>
<td align="left" width="63%">
Retrieves the underlying device GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecorderproperties">GetRecorderProperties</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface for the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecorderstate">GetRecorderState</a>
</td>
<td align="left" width="63%">
Checks if recorder is ready to burn.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-getrecordertype">GetRecorderType</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-openexclusive">OpenExclusive</a>
</td>
<td align="left" width="63%">
Opens a device for exclusive use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-querymediainfo">QueryMediaInfo</a>
</td>
<td align="left" width="63%">
Retrieves media properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-querymediatype">QueryMediaType</a>
</td>
<td align="left" width="63%">
Identifies the type of media in the recorder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscrecorder-setrecorderproperties">SetRecorderProperties</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nf-imapi-idiscmaster-setactivediscrecorder">IDiscMaster::SetActiveDiscRecorder</a> first.



