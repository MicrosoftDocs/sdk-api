---
UID: NF:winscard.SCardAddReaderToGroupA
title: SCardAddReaderToGroupA function (winscard.h)
description: Adds a reader to a reader group. (ANSI)
helpviewer_keywords: ["SCARD_ALL_READERS", "SCARD_DEFAULT_READERS", "SCARD_LOCAL_READERS", "SCARD_SYSTEM_READERS", "SCardAddReaderToGroupA", "winscard/SCardAddReaderToGroupA"]
old-location: security\scardaddreadertogroup.htm
tech.root: security
ms.assetid: f2f5fcd8-3b60-4c8a-b92c-c63be970cc35
ms.date: 12/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardAddReaderToGroup, SCardAddReaderToGroup function [Security], SCardAddReaderToGroupA, SCardAddReaderToGroupW, _smart_scardaddreadertogroup, security.scardaddreadertogroup, winscard/SCardAddReaderToGroup, winscard/SCardAddReaderToGroupA, winscard/SCardAddReaderToGroupW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardAddReaderToGroupW (Unicode) and SCardAddReaderToGroupA (ANSI)
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
 - SCardAddReaderToGroupA
 - winscard/SCardAddReaderToGroupA
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
 - SCardAddReaderToGroup
 - SCardAddReaderToGroupA
 - SCardAddReaderToGroupW
---

# SCardAddReaderToGroupA function


## -description

The <b>SCardAddReaderToGroup</b> function adds a <a href="/windows/desktop/SecGloss/r-gly">reader</a> to a <a href="/windows/desktop/SecGloss/r-gly">reader group</a>.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szReaderName [in]

Display name of the reader that you are adding.

### -param szGroupName [in]

Display name of the group to which you are adding the reader.

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

<b>SCardAddReaderToGroup</b> automatically creates the reader group specified if it does not already exist. 

The <b>SCardAddReaderToGroup</b> function is a database management function. For more information on other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.


#### Examples

The following example demonstrates how to add a smart card reader to a    group.     The example assumes that lReturn is an existing variable of type <b>LONG</b>, that <i>hContext</i> is a valid handle received from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function, and that "MyReader" and "MyReaderGroup"  are known by the system through previous calls to the <a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadera">SCardIntroduceReader</a> and <a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadergroupa">SCardIntroduceReaderGroup</a> functions, respectively.


```cpp

lReturn = SCardAddReaderToGroup( hContext, 
                                L"MyReader",
                                L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardAddReaderToGroup\n");

```






> [!NOTE]
> The winscard.h header defines SCardAddReaderToGroup as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadera">SCardIntroduceReader</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadergroupa">SCardIntroduceReaderGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardremovereaderfromgroupa">SCardRemoveReaderFromGroup</a>
