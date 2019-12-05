---
UID: NS:ddrawint._DD_GETVPORTSIGNALDATA
title: DD_GETVPORTSIGNALDATA (ddrawint.h)
description: The DD_GETVPORTSIGNALDATA structure contains the signal status of the hardware video port.
old-location: display\dd_getvportsignaldata.htm
tech.root: display
ms.assetid: 33db5ce5-534b-4e66-853b-5e60892f544b
ms.date: 12/05/2018
ms.keywords: '*PDD_GETVPORTSIGNALDATA, DD_GETVPORTSIGNALDATA, DD_GETVPORTSIGNALDATA structure [Display Devices], ddrawint/DD_GETVPORTSIGNALDATA, ddstrcts_4079ddf7-58a7-46ef-b11a-858bbd486333.xml, display.dd_getvportsignaldata'
ms.topic: struct
f1_keywords:
- ddrawint/DD_GETVPORTSIGNALDATA
dev_langs:
- c++
req.header: ddrawint.h
req.include-header: Winddi.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- ddrawint.h
api_name:
- DD_GETVPORTSIGNALDATA
targetos: Windows
req.typenames: '*PDD_GETVPORTSIGNALDATA, DD_GETVPORTSIGNALDATA'
req.redist: 
ms.custom: 19H1
---

# DD_GETVPORTSIGNALDATA structure


## -description


The DD_GETVPORTSIGNALDATA structure contains the signal status of the hardware video port.


## -struct-fields




### -field lpDD

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_local">DD_DIRECTDRAW_LOCAL</a> structure that is relevant to the current Microsoft DirectDraw process only.


### -field lpVideoPort

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoport_local">DD_VIDEOPORT_LOCAL</a> structure that represents this <a href="https://docs.microsoft.com/windows-hardware/drivers/">video port extensions (VPE)</a> object.


### -field dwStatus

Specifies the location in which the driver should write the status of the signal at the hardware video port. This member can be one of the following values:

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
DDVPSQ_NOSIGNAL

</td>
<td>
No video signal is present at the hardware video port.

</td>
</tr>
<tr>
<td>
DDVPSQ_SIGNALOK

</td>
<td>
A valid video signal is present at the hardware video port.

</td>
</tr>
</table>
 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getsignalstatus">DdVideoPortGetSignalStatus</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://docs.microsoft.com/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.


### -field GetVideoSignalStatus

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_vportcb_getsignalstatus">DdVideoPortGetSignalStatus</a>
 

 

