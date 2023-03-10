---
UID: NS:ddrawi._DDHAL_WAITFORVERTICALBLANKDATA
title: DDHAL_WAITFORVERTICALBLANKDATA (ddrawi.h)
description: The DD_WAITFORVERTICALBLANKDATA structure contains information necessary to obtain the monitor's vertical blank information. (DDHAL_WAITFORVERTICALBLANKDATA)
helpviewer_keywords: ["*LPDDHAL_WAITFORVERTICALBLANKDATA","DDHAL_WAITFORVERTICALBLANKDATA","DDHAL_WAITFORVERTICALBLANKDATA structure [Display Devices]","DD_WAITFORVERTICALBLANKDATA","DD_WAITFORVERTICALBLANKDATA structure [Display Devices]","ddrawint/DD_WAITFORVERTICALBLANKDATA","ddstrcts_cd09b34a-249c-4166-8624-bb638cf4bfe1.xml","display.dd_waitforverticalblankdata"]
old-location: display\dd_waitforverticalblankdata.htm
tech.root: display
ms.assetid: 27224fb2-3843-4843-b66f-0a3dd8325e1f
ms.date: 12/05/2018
ms.keywords: '*LPDDHAL_WAITFORVERTICALBLANKDATA, DDHAL_WAITFORVERTICALBLANKDATA, DDHAL_WAITFORVERTICALBLANKDATA structure [Display Devices], DD_WAITFORVERTICALBLANKDATA, DD_WAITFORVERTICALBLANKDATA structure [Display Devices], ddrawint/DD_WAITFORVERTICALBLANKDATA, ddstrcts_cd09b34a-249c-4166-8624-bb638cf4bfe1.xml, display.dd_waitforverticalblankdata'
req.header: ddrawi.h
req.include-header: Winddi.h, Ddrawi.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: '*LPDDHAL_WAITFORVERTICALBLANKDATA, DDHAL_WAITFORVERTICALBLANKDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DDHAL_WAITFORVERTICALBLANKDATA
 - ddrawi/_DDHAL_WAITFORVERTICALBLANKDATA
 - LPDDHAL_WAITFORVERTICALBLANKDATA
 - ddrawi/LPDDHAL_WAITFORVERTICALBLANKDATA
 - DDHAL_WAITFORVERTICALBLANKDATA
 - ddrawi/DDHAL_WAITFORVERTICALBLANKDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DDHAL_WAITFORVERTICALBLANKDATA
---

# DDHAL_WAITFORVERTICALBLANKDATA structure


## -description

The DD_WAITFORVERTICALBLANKDATA structure contains information necessary to obtain the monitor's vertical blank information.

## -struct-fields

### -field lpDD

Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field dwFlags

Specifies how the driver should wait for the vertical blank. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDWAITVB_BLOCKBEGIN

</td>
<td>
The driver should return when it detects the beginning of the vertical blank interval.

</td>
</tr>
<tr>
<td>
DDWAITVB_BLOCKBEGINEVENT

</td>
<td>
Set up an event to trigger when the vertical blank begins. This flag is not currently supported.

</td>
</tr>
<tr>
<td>
DDWAITVB_BLOCKEND

</td>
<td>
The driver should return when it detects the end of the vertical blank interval and display begins.

</td>
</tr>
<tr>
<td>
DDWAITVB_I_TESTVB

</td>
<td>
The driver should determine whether a vertical blank is currently occurring and return the status in <b>bIsInVB</b>.

</td>
</tr>
</table>

### -field bIsInVB

Indicates the status of the vertical blank. A value of <b>TRUE</b> indicates that the device is in a vertical blank; <b>FALSE</b> means that it is not. The driver should return the current vertical blanking status in this member when <b>dwFlags</b> is DDWAITVB_I_TESTVB.

### -field hEvent

Handle for the event that should be triggered when the vertical blank begins. The event is triggered on an interrupt, so if your hardware is able to generate an interrupt on the vertical blank, you should pass this event handle to your <a href="/windows-hardware/drivers/ddi/content/video/nc-video-pvideo_hw_interrupt">HwVidInterrupt</a> function so that the event is triggered when the interrupt fires. This member is currently unsupported and should be ignored by the driver.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_waitforverticalblank">DdWaitForVerticalBlank</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field WaitForVerticalBlank

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_waitforverticalblank">DdWaitForVerticalBlank</a>
