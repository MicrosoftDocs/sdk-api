---
UID: NF:mmiscapi.SendDriverMessage
title: SendDriverMessage function
author: windows-sdk-content
description: Sends the specified message to the installable driver.
old-location: multimedia\senddrivermessage.htm
tech.root: Multimedia
ms.assetid: 4787ccb7-3a32-4d55-9a3b-183e2f70735a
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: DRV_CONFIGURE, DRV_INSTALL, DRV_QUERYCONFIGURE, DRV_REMOVE, ISendDriverMessage, SendDriverMessage, SendDriverMessage function [Windows Multimedia], _win32_SendDriverMessage, mmsystem/SendDriverMessage, multimedia.senddrivermessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SendDriverMessage function


## -description


Sends the specified message to the installable driver.


## -parameters




### -param hDriver [in]

Handle of the installable driver instance. The handle must been previously created by using the <a href="https://msdn.microsoft.com/882146f7-cd42-45fd-8a5f-7078b64c7ea8">OpenDriver</a> function.


### -param message [in]

Driver message value. It can be a custom message value or one of these standard message values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DRV_QUERYCONFIGURE"></a><a id="drv_queryconfigure"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc">DRV_QUERYCONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Queries an installable driver about whether it supports the <b>DRV_CONFIGURE</b> message and can display a configuration dialog box.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_CONFIGURE"></a><a id="drv_configure"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/0d99fad7-ce79-4574-9fd8-262f7e758866">DRV_CONFIGURE</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies an installable driver that it should display a configuration dialog box. (This message should only be sent if the driver returns a nonzero value when the <a href="https://msdn.microsoft.com/fb2e36a7-8d6b-4b08-b2d7-e128ca7082dc">DRV_QUERYCONFIGURE</a> message is processed.)

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_INSTALL"></a><a id="drv_install"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/8ee7b30b-600b-49f3-93a7-8faa7b87cfd8">DRV_INSTALL</a></b></dt>
</dl>
</td>
<td width="60%">
Notifies an installable driver that it has been successfully installed.

</td>
</tr>
<tr>
<td width="40%"><a id="DRV_REMOVE"></a><a id="drv_remove"></a><dl>
<dt><b><a href="https://msdn.microsoft.com/e4f6ce7c-29e5-4256-b08a-13571256207c">DRV_REMOVE</a></b></dt>
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




<a href="https://msdn.microsoft.com/f3acbfa0-66d4-452b-b1df-ef6b46d1eb39">Installable Driver Functions</a>



<a href="https://msdn.microsoft.com/8b628a4d-48fa-4388-9d7c-0c901c45b7f3">Installable Drivers</a>
 

 

