---
UID: NF:prntvpt.PTGetPrintDeviceResources
title: PTGetPrintDeviceResources function (prntvpt.h)
description: It retrieves the print devices resources for a printer formatted in compliance with the XML Print Schema.
helpviewer_keywords: ["PTGetPrintDeviceResources","PTGetPrintDeviceResources function [XPS Documents and Packaging]","prntvpt/PTGetPrintDeviceResources","xps.ptgetprintdeviceresources"]
old-location: xps\ptgetprintdeviceresources.htm
tech.root: xps
ms.assetid: 39F17562-B8EB-41AF-BA55-42FE35B4560F
ms.date: 12/05/2018
ms.keywords: PTGetPrintDeviceResources, PTGetPrintDeviceResources function [XPS Documents and Packaging], prntvpt/PTGetPrintDeviceResources, xps.ptgetprintdeviceresources
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
 - PTGetPrintDeviceResources
 - prntvpt/PTGetPrintDeviceResources
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - prntvpt.dll
api_name:
 - PTGetPrintDeviceResources
---

# PTGetPrintDeviceResources function


## -description

It retrieves the print devices resources for a printer formatted in compliance with the XML <a href="/windows/desktop/printdocs/printschema">Print Schema</a>.

## -parameters

### -param hProvider [in]

A handle to an open device provider whose print device resources are to be retrieved. This handle is returned by the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenprovider">PTOpenProvider</a> or the <a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex">PTOpenProviderEx</a> function.

### -param pszLocaleName [in]

Optional pointer to the locale name. This parameter can be <b>NULL</b>.

### -param pPrintTicket [in]

A pointer to a stream with its seek position at the beginning of the print ticket content. This parameter can be <b>NULL</b>.

### -param pDeviceResources

A pointer to the stream where the device print resources will be written, starting at the current seek position.

### -param pbstrErrorMessage [out, optional]

A pointer to a PDC file or string that specifies what, if anything, is invalid about <i>pPrintTicket</i>. If it is valid, this value is <b>NULL</b>.

## -returns

If the operation succeeds, the return value is S_OK. Otherwise, returns an error message.

## -see-also

<a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities">PTGetPrintCapabilities</a>



<a href="/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintdevicecapabilities">PTGetPrintDeviceCapabilities</a>