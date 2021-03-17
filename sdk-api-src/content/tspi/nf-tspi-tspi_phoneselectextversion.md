---
UID: NF:tspi.TSPI_phoneSelectExtVersion
title: TSPI_phoneSelectExtVersion function (tspi.h)
description: The TSPI_phoneSelectExtVersion function selects the indicated extension version for the indicated phone device. Subsequent requests operate according to that extension version.
helpviewer_keywords: ["TSPI_phoneSelectExtVersion","TSPI_phoneSelectExtVersion function [TAPI 2.2]","_tspi_tspi_phoneselectextversion","tspi.tspi_phoneselectextversion","tspi/TSPI_phoneSelectExtVersion"]
old-location: tspi\tspi_phoneselectextversion.htm
tech.root: tapi3
ms.assetid: edd746c8-3d76-4759-b2a7-9ec75dd16842
ms.date: 12/05/2018
ms.keywords: TSPI_phoneSelectExtVersion, TSPI_phoneSelectExtVersion function [TAPI 2.2], _tspi_tspi_phoneselectextversion, tspi.tspi_phoneselectextversion, tspi/TSPI_phoneSelectExtVersion
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
 - TSPI_phoneSelectExtVersion
 - tspi/TSPI_phoneSelectExtVersion
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
 - TSPI_phoneSelectExtVersion
---

# TSPI_phoneSelectExtVersion function


## -description

The 
<b>TSPI_phoneSelectExtVersion</b> function selects the indicated extension version for the indicated phone device. Subsequent requests operate according to that extension version.

## -parameters

### -param hdPhone

The handle to the phone for which an extension version is to be selected.

### -param dwExtVersion

The extension version to be selected. This version number is negotiated using 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>. The most-significant <b>WORD</b> is the major version number and the least-significant <b>WORD</b> is the minor version number. Calling this function with a <i>dwExtVersion</i> of zero cancels the current selection.

## -returns

Returns zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

PHONEERR_INCOMPATIBLEEXTVERSION, PHONEERR_OPERATIONFAILED, PHONEERR_NOMEM, PHONEERR_OPERATIONUNAVAIL, PHONEERR_RESOURCEUNAVAIL.

## -remarks

This function selects the indicated extension version. Although the indicated version number may have been successfully negotiated, a different extension version may have been selected in the interim, in which case this function fails (returning PHONEERR_INCOMPATIBLEEXTVERSION).

Subsequent operations on the phone after an extension version is selected behave according to that extension version. Subsequent attempts to negotiate the extension version report strictly the selected version or zero (if the requested range does not include the selected version). Calling this procedure with the special extension version 0 cancels the current selection. The device once again becomes capable of supporting its full range of extension version numbers.

<b>TSPI_phoneSelectExtVersion</b> is typically called in two situations: (1) An application requested to open a phone, the application requested that a particular extension version be used, and no extension version was currently selected; or (2) the last application using a particular extension version closed the phone, and the extension version selection can be canceled.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonenegotiateextversion">TSPI_phoneNegotiateExtVersion</a>