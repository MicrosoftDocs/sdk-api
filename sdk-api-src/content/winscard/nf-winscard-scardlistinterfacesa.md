---
UID: NF:winscard.SCardListInterfacesA
title: SCardListInterfacesA function (winscard.h)
description: Provides a list of interfaces supplied by a given card. (ANSI)
helpviewer_keywords: ["SCardListInterfacesA", "winscard/SCardListInterfacesA"]
old-location: security\scardlistinterfaces.htm
tech.root: security
ms.assetid: 2460c133-3ad4-4f73-9f55-56fc3bab9cdb
ms.date: 12/05/2018
ms.keywords: SCardListInterfaces, SCardListInterfaces function [Security], SCardListInterfacesA, SCardListInterfacesW, _smart_scardlistinterfaces, security.scardlistinterfaces, winscard/SCardListInterfaces, winscard/SCardListInterfacesA, winscard/SCardListInterfacesW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardListInterfacesW (Unicode) and SCardListInterfacesA (ANSI)
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
 - SCardListInterfacesA
 - winscard/SCardListInterfacesA
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
 - SCardListInterfaces
 - SCardListInterfacesA
 - SCardListInterfacesW
---

# SCardListInterfacesA function


## -description

The <b>SCardListInterfaces</b> function provides a list of interfaces supplied by a given card.

The caller supplies the name of a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> previously introduced to the subsystem, and receives the list of interfaces supported by the card.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szCard [in]

Name of the smart card already introduced to the <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a>.

### -param pguidInterfaces [out]

Array of interface identifiers (GUIDs) that indicate the interfaces supported by the smart card. If this value is <b>NULL</b>, <b>SCardListInterfaces</b> ignores the array length supplied in <i>pcguidInterfaces</i>, returning the size of the array that would have been returned if this parameter had not been <b>NULL</b> to <i>pcguidInterfaces</i> and a success code.

### -param pcguidInterfaces [in, out]

Size of the <i>pcguidInterfaces</i> array, and receives the actual size of the returned array. If the array size is specified as SCARD_AUTOALLOCATE, then <i>pcguidInterfaces</i> is converted to a pointer to a GUID pointer, and receives the address of a block of memory containing the array. This block of memory must be deallocated with 
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

This function is not redirected, but calling the function when attempting a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardListInterfaces</b> function is a database query function. For more information on other database query functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-query-functions">Smart Card Database Query Functions</a>.


#### Examples

The following example  shows listing the interfaces for a smart card.


```cpp
LPGUID          pGuids = NULL;
LONG            lReturn;
DWORD           cGuid = SCARD_AUTOALLOCATE;

// Retrieve the list of interfaces.
lReturn = SCardListInterfaces(NULL,
                              (LPCSTR) "MyCard",
                              (LPGUID)&pGuids,
                              &cGuid );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardListInterfaces\n");
    exit(1);   // Or other appropriate action
}

if ( 0 != cGuid )
{
    // Do something with the array of Guids.
    // Remember to free pGuids when done (by SCardFreeMemory).
    // ...
}

```






> [!NOTE]
> The winscard.h header defines SCardListInterfaces as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardfreememory">SCardFreeMemory</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardgetproviderida">SCardGetProviderId</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadergroupsa">SCardListReaderGroups</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistreadersa">SCardListReaders</a>
