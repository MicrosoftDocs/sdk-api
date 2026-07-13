---
UID: NF:winscard.SCardForgetReaderGroupW
title: SCardForgetReaderGroupW function (winscard.h)
description: Removes a previously introduced smart card reader group from the smart card subsystem. Although this function automatically clears all readers from the group, it does not affect the existence of the individual readers in the database. (Unicode)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardForgetReaderGroup", "SCardForgetReaderGroup function [Security]", "SCardForgetReaderGroupW", "_smart_scardforgetreadergroup", "security.scardforgetreadergroup", "winscard/SCardForgetReaderGroup", "winscard/SCardForgetReaderGroupW"]
old-location: security\scardforgetreadergroup.htm
tech.root: security
ms.assetid: c6c98542-01b6-4b23-88cf-a619faee882e
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardForgetReaderGroup, SCardForgetReaderGroup function [Security], SCardForgetReaderGroupA, SCardForgetReaderGroupW, _smart_scardforgetreadergroup, security.scardforgetreadergroup, winscard/SCardForgetReaderGroup, winscard/SCardForgetReaderGroupA, winscard/SCardForgetReaderGroupW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardForgetReaderGroupW (Unicode) and SCardForgetReaderGroupA (ANSI)
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
 - SCardForgetReaderGroupW
 - winscard/SCardForgetReaderGroupW
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
 - SCardForgetReaderGroup
 - SCardForgetReaderGroupA
 - SCardForgetReaderGroupW
---

# SCardForgetReaderGroupW function


## -description

The <b>SCardForgetReaderGroup</b> function removes a previously introduced <a href="/windows/desktop/SecGloss/s-gly">smart card</a> <a href="/windows/desktop/SecGloss/r-gly">reader group</a> from the <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a>. Although this function automatically clears all readers from the group, it does not affect the existence of the individual <a href="/windows/desktop/SecGloss/r-gly">readers</a> in the database.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szGroupName [in]

Display name of the reader group to be removed. System-defined reader groups cannot be removed from the database.

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

The <b>SCardForgetReaderGroup</b> function is a database management function. For more information on other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.


#### Examples

The following example shows how to remove a reader group from the system. The example assumes that lReturn is an existing variable of type <b>LONG</b>, and that hContext is a valid handle to a resource manager context previously obtained from a call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function.


```cpp

lReturn = SCardForgetReaderGroup(hContext, 
                                 L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetReaderGroup\n");

```






> [!NOTE]
> The winscard.h header defines SCardForgetReaderGroup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetcardtypea">SCardForgetCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadera">SCardForgetReader</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadergroupa">SCardIntroduceReaderGroup</a>
