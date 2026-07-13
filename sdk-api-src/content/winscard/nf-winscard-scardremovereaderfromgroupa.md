---
UID: NF:winscard.SCardRemoveReaderFromGroupA
title: SCardRemoveReaderFromGroupA function (winscard.h)
description: Removes a reader from an existing reader group. This function has no effect on the reader. (ANSI)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardRemoveReaderFromGroupA", "winscard/SCardRemoveReaderFromGroupA"]
old-location: security\scardremovereaderfromgroup.htm
tech.root: security
ms.assetid: a9bdaf16-1a6f-4a84-ab29-3d6df9003ff9
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardRemoveReaderFromGroup, SCardRemoveReaderFromGroup function [Security], SCardRemoveReaderFromGroupA, SCardRemoveReaderFromGroupW, _smart_scardremovereaderfromgroup, security.scardremovereaderfromgroup, winscard/SCardRemoveReaderFromGroup, winscard/SCardRemoveReaderFromGroupA, winscard/SCardRemoveReaderFromGroupW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardRemoveReaderFromGroupW (Unicode) and SCardRemoveReaderFromGroupA (ANSI)
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
 - SCardRemoveReaderFromGroupA
 - winscard/SCardRemoveReaderFromGroupA
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
 - SCardRemoveReaderFromGroup
 - SCardRemoveReaderFromGroupA
 - SCardRemoveReaderFromGroupW
---

# SCardRemoveReaderFromGroupA function


## -description

The <b>SCardRemoveReaderFromGroup</b> function removes a <a href="/windows/desktop/SecGloss/r-gly">reader</a> from an existing <a href="/windows/desktop/SecGloss/r-gly">reader group</a>. This function has no effect on the reader.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szReaderName [in]

Display name of the reader to be removed.

### -param szGroupName [in]

Display name of the group from which the reader should be removed.

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

When the last reader is removed from a group, the group is automatically forgotten.

The <b>SCardRemoveReaderFromGroup</b> function is a database management function. For information about other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.

To add a reader to a reader group, use 
<a href="/windows/desktop/api/winscard/nf-winscard-scardaddreadertogroupa">SCardAddReaderToGroup</a>.


#### Examples

The following example  shows how to remove a reader from the group.


```cpp
// Remove a reader from the group.
// lReturn is of type LONG.
// hContext was set by a previous call to SCardEstablishContext.
// The group is automatically forgotten if no readers remain in it.
lReturn = SCardRemoveReaderFromGroup(hContext, 
                                     L"MyReader",
                                     L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardRemoveReaderFromGroup\n");

```






> [!NOTE]
> The winscard.h header defines SCardRemoveReaderFromGroup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardaddreadertogroupa">SCardAddReaderToGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetcardtypea">SCardForgetCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadera">SCardForgetReader</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadergroupa">SCardForgetReaderGroup</a>
