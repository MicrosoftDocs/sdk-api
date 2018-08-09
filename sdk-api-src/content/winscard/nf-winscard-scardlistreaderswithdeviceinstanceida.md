---
UID: NF:winscard.SCardListReadersWithDeviceInstanceIdA
title: SCardListReadersWithDeviceInstanceIdA function
author: windows-sdk-content
description: Gets the list of readers that have provided a device instance identifier. This function does not affect the state of the reader.
old-location: security\scardlistreaderswithdeviceinstanceid.htm
old-project: secauthn
ms.assetid: D470A10B-B167-4BCA-9042-BF63B9A3A92F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SCardListReadersWithDeviceInstanceId, SCardListReadersWithDeviceInstanceId function [Security], SCardListReadersWithDeviceInstanceIdA, SCardListReadersWithDeviceInstanceIdW, security.scardgetreadernamefromdeviceinstanceid, security.scardlistreaderswithdeviceinstanceid, winscard/SCardListReadersWithDeviceInstanceId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCardListReadersWithDeviceInstanceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardListReadersWithDeviceInstanceIdA function


## -description


The <b>SCardListReadersWithDeviceInstanceId</b> function gets the list of readers that have provided a device instance identifier. This function does not affect the state of the reader.


## -parameters




### -param hContext [in]

Handle that identifies the resource manager context for the query. You can set the resource manager context by a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function. This parameter cannot be <b>NULL</b>.


### -param szDeviceInstanceId [in]

Device instance ID of the reader. You can get this value by calling the <a href="https://msdn.microsoft.com/306F1EAF-35A7-4449-802F-709667764737">SCardGetReaderDeviceInstanceId</a> function with the reader name or by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551106">SetupDiGetDeviceInstanceId</a> function from the DDK.


### -param mszReaders [out, optional]

A multi-string that contain the smart card readers within the supplied device instance identifier. If this value is <b>NULL</b>, then the function ignores the buffer length supplied in the <i>pcchReaders</i> parameter, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchReaders</i>, and returns a success code. 


### -param pcchReaders [in, out]

The length, in characters, of the <i>mszReaders</i> buffer. This parameter receives the actual length of the multiple-string structure, including all terminating null characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszReaders</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory that contains the multiple-string structure. When you have finished using this memory, deallocated it by using the <a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a> function. 


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
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



   This function is not redirected. Calling the <b>SCardListReadersWithDeviceInstanceId</b> function when inside a Remote Desktop session fails with the SCARD_E_READER_UNAVAILABLE error code.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
szDeviceInstanceIdcchReaderNameLONG     lReturn, lReturn2;

LPTSTR   pmszReaders = NULL;
LPTSTR   pReader = NULL;WCHAR
DWORD    cchReaderName = SCARD_AUTOALLOCATE;

// Retrieve the reader’s name from it’s device instance ID
// hContext was set by a previous call to SCardEstablishContext. 

// szDeviceInstanceId was obtained by calling SetupDiGetDeviceInstanceId
lReturn = SCardListReadersWithDeviceInstanceId (hContext,
                         szDeviceInstanceId,
                         (LPTSTR)&amp;pmszReaders,
                         &amp;cchReaderName);

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

</pre>
</td>
</tr>
</table></span></div>


