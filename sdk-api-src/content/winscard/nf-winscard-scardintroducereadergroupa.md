---
UID: NF:winscard.SCardIntroduceReaderGroupA
title: SCardIntroduceReaderGroupA function (winscard.h)
description: Introduces a reader group to the smart card subsystem. However, the reader group is not created until the group is specified when adding a reader to the smart card database. (ANSI)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardIntroduceReaderGroupA", "winscard/SCardIntroduceReaderGroupA"]
old-location: security\scardintroducereadergroup.htm
tech.root: security
ms.assetid: aaf7d2f9-71d5-42bb-a96f-71124be40aa3
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardIntroduceReaderGroup, SCardIntroduceReaderGroup function [Security], SCardIntroduceReaderGroupA, SCardIntroduceReaderGroupW, _smart_scardintroducereadergroup, security.scardintroducereadergroup, winscard/SCardIntroduceReaderGroup, winscard/SCardIntroduceReaderGroupA, winscard/SCardIntroduceReaderGroupW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardIntroduceReaderGroupW (Unicode) and SCardIntroduceReaderGroupA (ANSI)
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
 - SCardIntroduceReaderGroupA
 - winscard/SCardIntroduceReaderGroupA
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
 - SCardIntroduceReaderGroup
 - SCardIntroduceReaderGroupA
 - SCardIntroduceReaderGroupW
---

# SCardIntroduceReaderGroupA function


## -description

The <b>SCardIntroduceReaderGroup</b> function introduces a <a href="/windows/desktop/SecGloss/r-gly">reader group</a> to the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> subsystem. However, the reader group is not created until the group is specified when adding a reader to the <a href="/windows/desktop/SecGloss/s-gly">smart card database</a>.

## -parameters

### -param hContext [in]

Supplies the handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function. If this parameter is <b>NULL</b>, the scope of the resource manager is SCARD_SCOPE_SYSTEM.

### -param szGroupName [in]

Supplies the display name to be assigned to the new reader group.

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

The <b>SCardIntroduceReaderGroup</b> function is provided for PC/SC specification compatibility. Reader groups are not stored until a reader is added to the group.

The <b>SCardIntroduceReaderGroup</b> function is a database management function. For a description of other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.

To remove a reader group, use 
<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadergroupa">SCardForgetReaderGroup</a>.


#### Examples

The following example  shows introducing a smart card reader group.


```cpp
// Introduce the reader group.
// lReturn is of type LONG.
// hContext was set by a previous call to SCardEstablishContext.
lReturn = SCardIntroduceReaderGroup(hContext, 
                                    L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardIntroduceReaderGroup\n");

```






> [!NOTE]
> The winscard.h header defines SCardIntroduceReaderGroup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardaddreadertogroupa">SCardAddReaderToGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadergroupa">SCardForgetReaderGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducecardtypea">SCardIntroduceCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadera">SCardIntroduceReader</a>
