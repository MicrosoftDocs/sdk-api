---
UID: NF:winscard.SCardListReaderGroupsA
title: SCardListReaderGroupsA function (winscard.h)
description: Provides the list of reader groups that have previously been introduced to the system. (ANSI)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardListReaderGroupsA", "winscard/SCardListReaderGroupsA"]
old-location: security\scardlistreadergroups.htm
tech.root: security
ms.assetid: df01fa4b-8053-4d3a-ae2e-66eeb6583225
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardListReaderGroups, SCardListReaderGroups function [Security], SCardListReaderGroupsA, SCardListReaderGroupsW, _smart_scardlistreadergroups, security.scardlistreadergroups, winscard/SCardListReaderGroups, winscard/SCardListReaderGroupsA, winscard/SCardListReaderGroupsW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardListReaderGroupsW (Unicode) and SCardListReaderGroupsA (ANSI)
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
 - SCardListReaderGroupsA
 - winscard/SCardListReaderGroupsA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardListReaderGroups
 - SCardListReaderGroupsA
 - SCardListReaderGroupsW
---

# SCardListReaderGroupsA function


## -description

The <b>SCardListReaderGroups</b> function provides the list of <a href="/windows/desktop/SecGloss/r-gly">reader groups</a> that have previously been introduced to the system.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. 

If this parameter is set to <b>NULL</b>, the search for reader groups is not limited to any context.

### -param mszGroups [out]

Multi-string that lists the reader groups defined to the system and available to the current user on the current <a href="/windows/desktop/SecGloss/t-gly">terminal</a>. If this value is <b>NULL</b>, <b>SCardListReaderGroups</b> ignores the buffer length supplied in <i>pcchGroups</i>, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchGroups</i>, and returns a success code.

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

### -param pcchGroups [in, out]

Length of the <i>mszGroups</i> buffer in characters, and receives the actual length of the multi-string structure, including all trailing <b>null</b> characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszGroups</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the multi-string structure. This block of memory must be deallocated with 
<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>.

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

A group is returned only if it contains at least one <a href="/windows/desktop/SecGloss/r-gly">reader</a>. This includes the group <a href="/windows/desktop/SecGloss/s-gly">SCard$DefaultReaders</a>. The group <a href="/windows/desktop/SecGloss/s-gly">SCard$AllReaders</a> cannot be returned, since it only exists implicitly.

The <b>SCardListReaderGroups</b> function is a database query function. For more information on other database query functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.


#### Examples

The following example  shows listing the reader groups.


```cpp
LPTSTR          pmszReaderGroups = NULL;
LPTSTR          pReaderGroup;
LONG            lReturn;
DWORD           cch = SCARD_AUTOALLOCATE;
    
// Retrieve the list the reader groups.
// hSC was set by a previous call to SCardEstablishContext.
lReturn = SCardListReaderGroups(hSC,
                                (LPTSTR)&pmszReaderGroups,
                                &cch );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardListReaderGroups\n");
else
{
    // Do something with the multi string of reader groups.
    // Output the values.
    // A double-null terminates the list of values.
    pReaderGroup = pmszReaderGroups;
    while ( '\0' != *pReaderGroup )
    {
        // Display the value.
        printf("%S\n", pReaderGroup );
        // Advance to the next value.
        pReaderGroup = pReaderGroup + wcslen((wchar_t *) pReaderGroup) + 1;
    }

    // Remember to free pmszReaderGroups by a call to SCardFreeMemory.
    // ...
}

```






> [!NOTE]
> The winscard.h header defines SCardListReaderGroups as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetproviderida">SCardGetProviderId</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistinterfacesa">SCardListInterfaces</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a>
