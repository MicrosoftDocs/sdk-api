---
UID: NF:winscard.SCardListReadersWithDeviceInstanceIdW
title: SCardListReadersWithDeviceInstanceIdW function (winscard.h)
description: Gets the list of readers that have provided a device instance identifier. This function does not affect the state of the reader. (Unicode)
helpviewer_keywords: ["SCardListReadersWithDeviceInstanceId", "SCardListReadersWithDeviceInstanceId function [Security]", "SCardListReadersWithDeviceInstanceIdW", "security.scardgetreadernamefromdeviceinstanceid", "security.scardlistreaderswithdeviceinstanceid", "winscard/SCardListReadersWithDeviceInstanceId"]
old-location: security\scardlistreaderswithdeviceinstanceid.htm
tech.root: security
ms.assetid: D470A10B-B167-4BCA-9042-BF63B9A3A92F
ms.date: 12/05/2018
ms.keywords: SCardListReadersWithDeviceInstanceId, SCardListReadersWithDeviceInstanceId function [Security], SCardListReadersWithDeviceInstanceIdA, SCardListReadersWithDeviceInstanceIdW, security.scardgetreadernamefromdeviceinstanceid, security.scardlistreaderswithdeviceinstanceid, winscard/SCardListReadersWithDeviceInstanceId
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
 - SCardListReadersWithDeviceInstanceIdW
 - winscard/SCardListReadersWithDeviceInstanceIdW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCardListReadersWithDeviceInstanceId
---

# SCardListReadersWithDeviceInstanceIdW function


## -description

The <b>SCardListReadersWithDeviceInstanceId</b> function gets the list of readers that have provided a device instance identifier. This function does not affect the state of the reader.

## -parameters

### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function. This parameter cannot be <b>NULL</b>.

### -param szDeviceInstanceId [in]

Device instance ID of the reader. You can get this value by calling the <a href="/windows/desktop/api/winscard/nf-winscard-scardgetreaderdeviceinstanceida">SCardGetReaderDeviceInstanceId</a> function with the reader name or by calling the <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdeviceinstanceida">SetupDiGetDeviceInstanceId</a> function from the DDK.

### -param mszReaders [out, optional]

A multi-string that contain the smart card readers within the supplied device instance identifier. If this value is <b>NULL</b>, then the function ignores the buffer length supplied in the <i>pcchReaders</i> parameter, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchReaders</i>, and returns a success code.

### -param pcchReaders [in, out]

The length, in characters, of the <i>mszReaders</i> buffer. This parameter receives the actual length of the multiple-string structure, including all terminating null characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszReaders</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory that contains the multiple-string structure. When you have finished using this memory, deallocated it by using the <a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a> function.

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

   This function is not redirected. Calling the <b>SCardListReadersWithDeviceInstanceId</b> function when inside a Remote Desktop session fails with the SCARD_E_READER_UNAVAILABLE error code.


#### Examples


```cpp

szDeviceInstanceIdcchReaderNameLONG     lReturn, lReturn2;

LPTSTR   pmszReaders = NULL;
LPTSTR   pReader = NULL;WCHAR
DWORD    cchReaderName = SCARD_AUTOALLOCATE;

// Retrieve the reader’s name from it’s device instance ID
// hContext was set by a previous call to SCardEstablishContext. 

// szDeviceInstanceId was obtained by calling SetupDiGetDeviceInstanceId
lReturn = SCardListReadersWithDeviceInstanceId (hContext,
                         szDeviceInstanceId,
                         (LPTSTR)&pmszReaders,
                         &cchReaderName);

switch( lReturn )
{
    case SCARD_E_NO_READERS_AVAILABLE:
        printf("No readers have the provided device instance ID.\n");
        // Take appropriate action.
        // ...
        break;

    case SCARD_S_SUCCESS:
        // Do something with the multi string of readers.
        // Output the values.
        // A double-null terminates the list of values.
        pReader = pmszReaders;
        while ( '\0' != *pReader )
        {
            // Display the value.
            printf("Reader: %S\n", pReader );
            // Advance to the next value.
            pReader = pReader + wcslen((wchar_t *)pReader) + 1;
        }
        // Free the memory.
        lReturn2 = SCardFreeMemory( hContext,
                                   pmszReaders );
        if ( SCARD_S_SUCCESS != lReturn2 )
            printf("Failed SCardFreeMemory\n");
        break;

default:
        printf("Failed SCardListReaders\n");
        // Take appropriate action.
        // ...
        break;


```





> [!NOTE]
> The winscard.h header defines SCardListReadersWithDeviceInstanceId as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
