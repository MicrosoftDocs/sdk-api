---
UID: NF:winscard.SCardListReadersA
title: SCardListReadersA function (winscard.h)
description: Provides the list of readers within a set of named reader groups, eliminating duplicates. (ANSI)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardListReadersA", "winscard/SCardListReadersA"]
old-location: security\scardlistreaders.htm
tech.root: security
ms.assetid: b50218f1-e960-4838-b44b-6c71fa94a0ad
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardListReaders, SCardListReaders function [Security], SCardListReadersA, SCardListReadersW, _smart_scardlistreaders, security.scardlistreaders, winscard/SCardListReaders, winscard/SCardListReadersA, winscard/SCardListReadersW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardListReadersW (Unicode) and SCardListReadersA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardListReadersA
 - winscard/SCardListReadersA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardListReaders
 - SCardListReadersA
 - SCardListReadersW
---

# SCardListReadersA function


## -description

The <b>SCardListReaders</b> function provides the list of <a href="/windows/desktop/SecGloss/r-gly">readers</a> within a set of named <a href="/windows/desktop/SecGloss/r-gly">reader groups</a>, eliminating duplicates.

The caller supplies a list of reader groups, and receives the list of readers within the named groups. Unrecognized group names are ignored. This function only returns readers within the named groups that are currently attached to the system and available for use.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. 

If this parameter is set to <b>NULL</b>, the search for readers is not limited to any context.

### -param mszGroups [in, optional]

Names of the reader groups defined to the system, as a multi-string. Use a <b>NULL</b> value to list all readers in the system (that is, the SCard$AllReaders group).

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ALL_READERS"></a><a id="scard_all_readers"></a><dl>
<dt><b>SCARD_ALL_READERS</b></dt>
<dt>TEXT("SCard$AllReaders\000")</dt>
</dl>
</td>
<td width="60%">
Group used when no group name is provided when listing readers. Returns a list of all readers, regardless of what group or groups the readers are in.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_DEFAULT_READERS"></a><a id="scard_default_readers"></a><dl>
<dt><b>SCARD_DEFAULT_READERS</b></dt>
<dt>TEXT("SCard$DefaultReaders\000")</dt>
</dl>
</td>
<td width="60%">
Default group to which all readers are added when introduced into the system.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_LOCAL_READERS"></a><a id="scard_local_readers"></a><dl>
<dt><b>SCARD_LOCAL_READERS</b></dt>
<dt>TEXT("SCard$LocalReaders\000")</dt>
</dl>
</td>
<td width="60%">
Unused legacy value. This is an internally managed group that cannot be modified by using any reader group APIs. It is intended to be used for enumeration only.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SYSTEM_READERS"></a><a id="scard_system_readers"></a><dl>
<dt><b>SCARD_SYSTEM_READERS</b></dt>
<dt>TEXT("SCard$SystemReaders\000")</dt>
</dl>
</td>
<td width="60%">
Unused legacy value. This is an internally managed group that cannot be modified by using any reader group APIs. It is intended to be used for enumeration only.

</td>
</tr>
</table>

### -param mszReaders [out]

Multi-string that lists the card readers within the supplied reader groups. If this value is <b>NULL</b>, <b>SCardListReaders</b> ignores the buffer length supplied in <i>pcchReaders</i>, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchReaders</i>, and returns a success code.

### -param pcchReaders [in, out]

Length of the <i>mszReaders</i> buffer in characters. This parameter receives the actual length of the multi-string structure, including all trailing <b>null</b> characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszReaders</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the multi-string structure. This block of memory must be deallocated with <a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>.

## -returns

This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Group contains no readers</b></dt>
<dt>2148532270 (0x8010002E)</dt>
</dl>
</td>
<td width="60%">
SCARD_E_NO_READERS_AVAILABLE

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Specified reader is not currently available for use</b></dt>
<dt>2148532247 (0x80100017)</dt>
</dl>
</td>
<td width="60%">
SCARD_E_READER_UNAVAILABLE

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>

## -remarks

The <b>SCardListReaders</b> function is a database query function. For more information on other database query functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.


#### Examples

The following example  shows listing the readers.


```cpp
LPTSTR          pmszReaders = NULL;
LPTSTR          pReader;
LONG            lReturn, lReturn2;
DWORD           cch = SCARD_AUTOALLOCATE;

// Retrieve the list the readers.
// hSC was set by a previous call to SCardEstablishContext.
lReturn = SCardListReaders(hSC,
                           NULL,
                           (LPTSTR)&pmszReaders,
                           &cch );
switch( lReturn )
{
    case SCARD_E_NO_READERS_AVAILABLE:
        printf("Reader is not in groups.\n");
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
        lReturn2 = SCardFreeMemory( hSC,
                                   pmszReaders );
        if ( SCARD_S_SUCCESS != lReturn2 )
            printf("Failed SCardFreeMemory\n");
        break;

default:
        printf("Failed SCardListReaders\n");
        // Take appropriate action.
        // ...
        break;
}

```






> [!NOTE]
> The winscard.h header defines SCardListReaders as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetproviderida">SCardGetProviderId</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistinterfacesa">SCardListInterfaces</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadergroupsa">SCardListReaderGroups</a>
