---
UID: NF:batclass.BatteryClassSystemControl
title: BatteryClassSystemControl function (batclass.h)
description: The BatteryClassSystemControl routine processes WMI IRPs on behalf of a battery miniclass driver.
helpviewer_keywords: ["BatteryClassSystemControl","BatteryClassSystemControl routine [Battery Devices]","bat-rtn_4e2bda63-ff7a-420f-96af-fa0d5041479b.xml","batclass/BatteryClassSystemControl","battery.batteryclasssystemcontrol"]
old-location: battery\batteryclasssystemcontrol.htm
tech.root: battery
ms.assetid: d462c51d-e175-4fc8-88b9-515ba648fab4
ms.date: 12/05/2018
ms.keywords: BatteryClassSystemControl, BatteryClassSystemControl routine [Battery Devices], bat-rtn_4e2bda63-ff7a-420f-96af-fa0d5041479b.xml, batclass/BatteryClassSystemControl, battery.batteryclasssystemcontrol
req.header: batclass.h
req.include-header: Batclass.h
req.target-type: Desktop
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
req.lib: Battc.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BatteryClassSystemControl
 - batclass/BatteryClassSystemControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Battc.lib
 - Battc.dll
api_name:
 - BatteryClassSystemControl
---

# BatteryClassSystemControl function


## -description

The <b>BatteryClassSystemControl</b> routine processes WMI IRPs on behalf of a battery miniclass driver.

## -parameters

### -param ClassData [in]

Pointer to a battery class handle that was previously received from <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassinitializedevice">BatteryClassInitializeDevice</a>.

### -param WmiLibContext [in]

Pointer to a <a href="/windows-hardware/drivers/ddi/content/wmilib/ns-wmilib-_wmilib_context">WMILIB_CONTEXT</a> structure.  The structure provides WMI registration information, and dispatch routines for driver-specific WMI request processing.

### -param DeviceObject [in]

Pointer to the driver's device object.

### -param Irp [in, out]

Pointer to the IRP that contains the WMI request.

### -param Disposition [out]

Pointer to a memory location that the routine uses to return information about how it handled the IRP.  See <a href="/windows-hardware/drivers/ddi/content/wmilib/nf-wmilib-wmisystemcontrol">WmiSystemControl</a> for a description of the possible values returned.

## -returns

<b>BatteryClassSystemControl</b> returns STATUS_SUCCESS on success, and the appropriate error code on failure.

## -remarks

Battery miniclass drivers must call this routine instead of <a href="/windows-hardware/drivers/ddi/content/wmilib/nf-wmilib-wmisystemcontrol">WmiSystemControl</a>.  It provides the same functionality as <b>WmiSystemControl</b>, but it also ensures that the driver registers the WMI classes that the battery class driver handles on behalf of the miniclass driver.

A battery miniclass driver's <a href="/windows-hardware/drivers/ddi/content/wmilib/nc-wmilib-wmi_query_datablock_callback">DpWmiQueryDataBlock</a> routine, which is specified by the <b>QueryWmiDataBlock</b> member of <a href="/windows-hardware/drivers/ddi/content/wmilib/ns-wmilib-_wmilib_context">WMILIB_CONTEXT</a>, must call the <a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a> routine to allow the battery class driver to process the query for the WMI classes it handles on behalf of the miniclass driver.

## -see-also

<a href="/windows/desktop/api/batclass/nf-batclass-batteryclassquerywmidatablock">BatteryClassQueryWmiDataBlock</a>



<a href="/windows-hardware/drivers/ddi/content/wmilib/nc-wmilib-wmi_query_datablock_callback">DpWmiQueryDataBlock</a>



<a href="/windows-hardware/drivers/ddi/content/wmilib/ns-wmilib-_wmilib_context">WMILIB_CONTEXT</a>