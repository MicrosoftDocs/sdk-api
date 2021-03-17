---
UID: NF:tspi.TSPI_lineSelectExtVersion
title: TSPI_lineSelectExtVersion function (tspi.h)
description: The TSPI_lineSelectExtVersion function selects the indicated extension version for the indicated line device. Subsequent requests operate according to that extension version.
helpviewer_keywords: ["TSPI_lineSelectExtVersion","TSPI_lineSelectExtVersion function [TAPI 2.2]","_tspi_tspi_lineselectextversion","tspi.tspi_lineselectextversion","tspi/TSPI_lineSelectExtVersion"]
old-location: tspi\tspi_lineselectextversion.htm
tech.root: tapi3
ms.assetid: 8c083afc-2e15-4260-ba67-84125c777cbf
ms.date: 12/05/2018
ms.keywords: TSPI_lineSelectExtVersion, TSPI_lineSelectExtVersion function [TAPI 2.2], _tspi_tspi_lineselectextversion, tspi.tspi_lineselectextversion, tspi/TSPI_lineSelectExtVersion
req.header: tspi.h
req.include-header: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineSelectExtVersion
 - tspi/TSPI_lineSelectExtVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineSelectExtVersion
---

# TSPI_lineSelectExtVersion function


## -description

The 
<b>TSPI_lineSelectExtVersion</b> function selects the indicated extension version for the indicated line device. Subsequent requests operate according to that extension version.

## -parameters

### -param hdLine

The handle to the line for which an extension version is to be selected.

### -param dwExtVersion

The extension version to be selected. This version number has been negotiated using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>. The most significant <b>WORD</b> is the major version number and the least significant <b>WORD</b> is the minor version number. Calling this function with a <i>dwExtVersion</i> of zero cancels the current selection.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INCOMPATIBLEEXTVERSION, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL, LINEERR_OPERATIONUNAVAIL.

## -remarks

The service provider selects the indicated extension version. Although the indicated version number may have been successfully negotiated, a different extension version may have been selected in the interim, in which case this function fails (returning LINEERR_INCOMPATIBLEEXTVERSION).

Subsequent operations on the line after an extension version has been selected behave according to that extension version. Subsequent attempts to negotiate the extension version report strictly the selected version or 0 (if the requested range does not include the selected version). Calling this procedure with the special extension version 0 cancels the current selection. The device becomes once again capable of supporting its full range of extension version numbers.

This function has no direct correspondence at the TAPI level, where selecting an extension version is bundled with the other functionality of 
<a href="/windows/desktop/api/tapi/nf-tapi-lineopen">lineOpen</a>. The 
<b>TSPI_lineSelectExtVersion</b> function is typically called in two situations: (1) An application requested to open a line, the resulting change of media type monitoring was successful, the application requested that a particular extension version be used, and no extension version was currently selected. (2) The last application using a particular extension version closed the line, and the extension version selection can be canceled.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linenegotiateextversion">TSPI_lineNegotiateExtVersion</a>