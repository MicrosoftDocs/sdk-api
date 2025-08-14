---
UID: NF:winscard.SCardGetDeviceTypeIdW
title: SCardGetDeviceTypeIdW function (winscard.h)
description: Gets the device type identifier of the card reader for the given reader name. This function does not affect the state of the reader. (Unicode)
helpviewer_keywords: ["SCardGetDeviceTypeId", "SCardGetDeviceTypeId function [Security]", "SCardGetDeviceTypeIdW", "security.scardgetdevicetypeid", "winscard/SCardGetDeviceTypeId", "winscard/SCardGetDeviceTypeIdW"]
old-location: security\scardgetdevicetypeid.htm
tech.root: security
ms.assetid: E637B5D6-B605-4216-9581-7E4ADC75F75A
ms.date: 12/05/2018
ms.keywords: SCardGetDeviceTypeId, SCardGetDeviceTypeId function [Security], SCardGetDeviceTypeIdA, SCardGetDeviceTypeIdW, security.scardgetdevicetypeid, winscard/SCardGetDeviceTypeId, winscard/SCardGetDeviceTypeIdA, winscard/SCardGetDeviceTypeIdW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetDeviceTypeIdW (Unicode) and SCardGetDeviceTypeIdA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardGetDeviceTypeIdW
 - winscard/SCardGetDeviceTypeIdW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - ext-ms-win-security-winscard-l1-1-0.dll
 - Winscard.dll
api_name:
 - SCardGetDeviceTypeId
 - SCardGetDeviceTypeIdA
 - SCardGetDeviceTypeIdW
---

# SCardGetDeviceTypeIdW function


## -description

The <b>SCardGetDeviceTypeId</b> function gets the device type identifier of the card reader for the given reader name. This function does not affect the state of the reader.

## -parameters

### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by calling the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function. This parameter cannot be NULL.

### -param szReaderName [in]

Reader name. You can get this value by calling the <a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a> function.

### -param pdwDeviceTypeId [in, out]

The actual device type identifier. The list of reader types returned by this function are listed under <b>ReaderType</b> member in the <a href="/windows-hardware/drivers/ddi/content/smclib/ns-smclib-_scard_reader_capabilities">SCARD_READER_CAPABILITIES</a> structure.

## -returns

This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The winscard.h header defines SCardGetDeviceTypeId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
