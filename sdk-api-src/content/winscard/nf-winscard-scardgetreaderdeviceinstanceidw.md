---
UID: NF:winscard.SCardGetReaderDeviceInstanceIdW
title: SCardGetReaderDeviceInstanceIdW function (winscard.h)
description: Gets the device instance identifier of the card reader for the given reader name. This function does not affect the state of the reader. (Unicode)
helpviewer_keywords: ["SCardGetReaderDeviceInstanceId", "SCardGetReaderDeviceInstanceId function [Security]", "SCardGetReaderDeviceInstanceIdW", "security.scardgetreaderdeviceinstanceid", "winscard/SCardGetReaderDeviceInstanceId"]
old-location: security\scardgetreaderdeviceinstanceid.htm
tech.root: security
ms.assetid: 306F1EAF-35A7-4449-802F-709667764737
ms.date: 12/05/2018
ms.keywords: SCardGetReaderDeviceInstanceId, SCardGetReaderDeviceInstanceId function [Security], SCardGetReaderDeviceInstanceIdA, SCardGetReaderDeviceInstanceIdW, security.scardgetreaderdeviceinstanceid, winscard/SCardGetReaderDeviceInstanceId
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - SCardGetReaderDeviceInstanceIdW
 - winscard/SCardGetReaderDeviceInstanceIdW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ext-ms-win-security-winscard-l1-1-1.dll
 - Winscard.h
api_name:
 - SCardGetReaderDeviceInstanceId
---

# SCardGetReaderDeviceInstanceIdW function


## -description

The <b>SCardGetReaderDeviceInstanceId</b> function gets the device instance identifier of  the card reader for the given reader name. This function does not affect the state of the reader.

## -parameters

### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function. This parameter cannot be <b>NULL</b>.

### -param szReaderName [in]

Reader name. You can get this value by calling the <a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a> function.

### -param szDeviceInstanceId [out, optional]

Buffer that receives the device instance ID of the reader. If this value is <b>NULL</b>, the function ignores the buffer length supplied in <i>cchDeviceInstanceId</i> parameter, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>cchDeviceInstanceId</i>, and returns a success code.

### -param pcchDeviceInstanceId [in, out]

Length, in characters, of the <i>szDeviceInstanceId</i> buffer, including the <b>NULL</b> terminator. If the buffer length is specified as SCARD_AUTOALLOCATE, then the <i>szDeviceInstanceId</i> parameter is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the instance id. This block of memory must be deallocated with the <a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a> function.

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

   This function is not redirected. Calling the <b>SCardGetReaderDeviceInstanceId</b> function when inside a Remote Desktop session fails with the SCARD_E_READER_UNAVAILABLE error code.


#### Examples


```cpp

LONG     lReturn;
LPTSTR   szReaderName = "USB Smart Card Reader 0";
WCHAR    szDeviceInstanceId[256];
DWORD    cchDeviceInstanceId = 256;

// Retrieve the reader's device instance ID.
// hContext was set by a previous call to SCardEstablishContext.
lReturn = SCardGetReaderDeviceInstanceId (hContext,
                         szReaderName,
                         szDeviceInstanceId,
                         &cchDeviceInstanceId);

if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardGetReaderDeviceInstanceId - %x\n", lReturn);
    // Take appropriate action.
}



```





> [!NOTE]
> The winscard.h header defines SCardGetReaderDeviceInstanceId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
