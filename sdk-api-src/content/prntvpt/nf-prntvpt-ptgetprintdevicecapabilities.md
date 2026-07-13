---
UID: NF:prntvpt.PTGetPrintDeviceCapabilities
title: PTGetPrintDeviceCapabilities function (prntvpt.h)
description: Retrieves the device printer's capabilities formatted in compliance with the XML Print Schema.
helpviewer_keywords: ["PTGetPrintDeviceCapabilities","PTGetPrintDeviceCapabilities function [XPS Documents and Packaging]","prntvpt/PTGetPrintDeviceCapabilities","xps.ptgetprintdevicecapabilities"]
old-location: xps\ptgetprintdevicecapabilities.htm
tech.root: xps
ms.assetid: DB9D63B1-2703-47F7-8F31-30FA0110E1E9
ms.date: 12/05/2018
ms.keywords: PTGetPrintDeviceCapabilities, PTGetPrintDeviceCapabilities function [XPS Documents and Packaging], prntvpt/PTGetPrintDeviceCapabilities, xps.ptgetprintdevicecapabilities
req.header: prntvpt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
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
req.lib: Prntvpt.lib
req.dll: Prntvpt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTGetPrintDeviceCapabilities
 - prntvpt/PTGetPrintDeviceCapabilities
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-printer-prntvpt-l1-1-2.dll
 - prntvpt.dll
api_name:
 - PTGetPrintDeviceCapabilities
---

# PTGetPrintDeviceCapabilities function


## -description

Retrieves the device printer's capabilities formatted in compliance with the XML <a href="/windows/desktop/printdocs/printschema">Print Schema</a>.

## -parameters

### -param hProvider [in]

A handle to an open device provider whose print capabilities are to be retrieved. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

### -param pPrintTicket [in, optional]

An optional pointer to a stream with its seek position at the beginning of the print ticket content. This parameter can be <b>NULL</b>.

### -param pDeviceCapabilities

A pointer to the stream where the device print capabilities will be written, starting at the current seek position.

### -param pbstrErrorMessage [out, optional]

A pointer to a PDC file or string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this value is <b>NULL</b>.The function uses this parameter only used if <i>pPrintTicket</i> is used.

## -returns

If the operation succeeds, the return value is S_OK. Otherwise, returns an error message.

## -see-also

<a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities">PTGetPrintCapabilities</a>