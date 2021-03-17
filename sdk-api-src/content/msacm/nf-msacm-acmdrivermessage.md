---
UID: NF:msacm.acmDriverMessage
title: acmDriverMessage function (msacm.h)
description: The acmDriverMessage function sends a user-defined message to a given ACM driver instance.
helpviewer_keywords: ["_win32_acmDriverMessage","acmDriverMessage","acmDriverMessage function [Windows Multimedia]","msacm/acmDriverMessage","multimedia.acmdrivermessage"]
old-location: multimedia\acmdrivermessage.htm
tech.root: Multimedia
ms.assetid: c4e1685e-54b5-4c33-b23c-c3ccc31afe48
ms.date: 12/05/2018
ms.keywords: _win32_acmDriverMessage, acmDriverMessage, acmDriverMessage function [Windows Multimedia], msacm/acmDriverMessage, multimedia.acmdrivermessage
req.header: msacm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Msacm32.lib
req.dll: Msacm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - acmDriverMessage
 - msacm/acmDriverMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msacm32.dll
 - Ext-MS-Win-mm-msacm-l1-1-0.dll
api_name:
 - acmDriverMessage
---

# acmDriverMessage function


## -description

The <b>acmDriverMessage</b> function sends a user-defined message to a given ACM driver instance.

## -parameters

### -param had

Handle to the ACM driver instance to which the message will be sent.

### -param uMsg

Message that the ACM driver must process. This message must be in the ACMDM_USER message range (above or equal to ACMDM_USER and less than ACMDM_RESERVED_LOW). The exceptions to this restriction are the ACMDM_DRIVER_ABOUT, <a href="/windows/desktop/Multimedia/drv-queryconfigure">DRV_QUERYCONFIGURE</a>, and <a href="/windows/desktop/Multimedia/drv-configure">DRV_CONFIGURE</a> messages.

### -param lParam1

Message parameter.

### -param lParam2

Message parameter.

## -returns

The return value is specific to the user-defined ACM driver message specified by the uMsg parameter. However, possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The <i>uMsg</i> parameter is not in the ACMDM_USER range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The ACM driver did not process the message.

</td>
</tr>
</table>

## -remarks

To display a custom About dialog box from an ACM driver, an application must send the ACMDM_DRIVER_ABOUT message to the driver. The <i>lParam1</i> parameter should be the handle of the owner window for the custom About dialog box, and <i>lParam2</i> must be set to zero. If the driver does not support a custom About dialog box, MMSYSERR_NOTSUPPORTED will be returned and it is the application's responsibility to display its own dialog box. For example, the Control Panel Sound Mapper option will display a default About dialog box based on the <b>ACMDRIVERDETAILS</b> structure when an ACM driver returns MMSYSERR_NOTSUPPORTED. An application can query a driver for custom About dialog box support without the dialog box being displayed by setting <i>lParam1</i> to –1L. If the driver supports a custom About dialog box, MMSYSERR_NOERROR will be returned. Otherwise, the return value is MMSYSERR_NOTSUPPORTED.

User-defined messages must be sent only to an ACM driver that specifically supports the messages. The caller should verify that the ACM driver is the correct driver by retrieving the driver details and checking the <b>wMid</b>, <b>wPid</b>, and <b>vdwDriver</b> members of the <b>ACMDRIVERDETAILS</b> structure.

Never send user-defined messages to an unknown ACM driver.

## -see-also

<a href="/windows/desktop/Multimedia/audio-compression-functions">Audio Compression Functions</a>



<a href="/windows/desktop/Multimedia/audio-compression-manager">Audio Compression Manager</a>