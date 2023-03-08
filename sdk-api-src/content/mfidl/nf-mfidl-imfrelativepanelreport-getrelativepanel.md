---
UID: NF:mfidl.IMFRelativePanelReport.GetRelativePanel
title: IMFRelativePanelReport::GetRelativePanel
ms.date: 11/4/2019
targetos: Windows
description: Gets a value from the ACPI_PLD_PANEL enumeration indicating the location of the capture device.
tech.root: mf
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFRelativePanelReport::GetRelativePanel
f1_keywords:
 - IMFRelativePanelReport::GetRelativePanel
 - mfidl/IMFRelativePanelReport::GetRelativePanel
dev_langs:
 - c++
---

## -description

Gets a value from the [ACPI_PLD_PANEL](/windows-hardware/drivers/ddi/acpitabl/ne-acpitabl-_acpi_pld_panel) enumeration indicating the location of the capture device, relative to the display provided to [MFCreateRelativePanelWatcher](nf-mfidl-mfcreaterelativepanelwatcher.md).

## -parameters

### -param panel

Receives a pointer to a **ULONG** value from the **ACPI_PLD_PANEL** enumeration.

## -returns

The function returns an **HRESULT**. Possible values include, but are not limited to, those in the following table.

| Return code | Description |
|--------------|------------------------|
|S_OK | The function succeeded.|

## -remarks

## -see-also

