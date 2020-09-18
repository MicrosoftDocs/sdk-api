---
UID: NF:mmiscapi.SendDriverMessage
title: SendDriverMessage function (mmiscapi.h)
description: Sends the specified message to the installable driver.
helpviewer_keywords: ["DRV_CONFIGURE","DRV_INSTALL","DRV_QUERYCONFIGURE","DRV_REMOVE","ISendDriverMessage","SendDriverMessage","SendDriverMessage function [Windows Multimedia]","_win32_SendDriverMessage","mmsystem/SendDriverMessage","multimedia.senddrivermessage"]
old-location: multimedia\senddrivermessage.htm
tech.root: Multimedia
ms.assetid: 4787ccb7-3a32-4d55-9a3b-183e2f70735a
ms.date: 12/05/2018
ms.keywords: DRV_CONFIGURE, DRV_INSTALL, DRV_QUERYCONFIGURE, DRV_REMOVE, ISendDriverMessage, SendDriverMessage, SendDriverMessage function [Windows Multimedia], _win32_SendDriverMessage, mmsystem/SendDriverMessage, multimedia.senddrivermessage
req.header: mmiscapi.h
req.include-header: Mmiscapi.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Installable Drivers, Installable Driver Functions
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SendDriverMessage
 - mmiscapi/SendDriverMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-misc-l1-1-0.dll
 - winmmbase.dll
 - API-MS-Win-mm-misc-l1-1-1.dll
api_name:
 - SendDriverMessage
---

# SendDriverMessage function


## -description

Sends the specified message to the installable driver.

## -parameters

### -param hDriver [in]

Handle of the installable driver instance. The handle must been previously created by using the <a href="/previous-versions/dd743639(v=vs.85)">OpenDriver</a> function.

### -param message [in]

Driver message value. It can be a custom message value or one of these standard message values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRV_QUERYCONFIGURE"></a><a id="drv_queryconfigure"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-queryconfigure">DRV_QUERYCONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Queries an installable driver about whether it supports the <b>DRV_CONFIGURE</b> message and can display a configuration dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_CONFIGURE"></a><a id="drv_configure"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies an installable driver that it should display a configuration dialog box. (This message should only be sent if the driver returns a nonzero value when the <a href="/windows/desktop/Multimedia/drv-queryconfigure">DRV_QUERYCONFIGURE</a> message is processed.)

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_INSTALL"></a><a id="drv_install"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-install">DRV_INSTALL</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies an installable driver that it has been successfully installed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_REMOVE"></a><a id="drv_remove"></a><dl>
<dt><b><a href="/windows/desktop/Multimedia/drv-remove">DRV_REMOVE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies an installable driver that it is about to be removed from the system.

</td>
</tr>
</table>

### -param lParam1 [in, out]

32-bit message-dependent information.

### -param lParam2 [in, out]

32-bit message-dependent information.

## -returns

Returns nonzero if successful or zero otherwise.

## -see-also

<a href="/windows/desktop/Multimedia/installable-driver-functions">Installable Driver Functions</a>



<a href="/windows/desktop/Multimedia/installable-drivers">Installable Drivers</a>