---
UID: NF:winscard.SCardForgetReaderW
title: SCardForgetReaderW function (winscard.h)
description: Removes a previously introduced reader from control by the smart card subsystem. It is removed from the smart card database, including from any reader group that it may have been added to. (Unicode)
helpviewer_keywords: ["SCardForgetReader", "SCardForgetReader function [Security]", "SCardForgetReaderW", "_smart_scardforgetreader", "security.scardforgetreader", "winscard/SCardForgetReader", "winscard/SCardForgetReaderW"]
old-location: security\scardforgetreader.htm
tech.root: security
ms.assetid: 2022caff-ba01-4d0d-977c-3f51bde95659
ms.date: 12/05/2018
ms.keywords: SCardForgetReader, SCardForgetReader function [Security], SCardForgetReaderA, SCardForgetReaderW, _smart_scardforgetreader, security.scardforgetreader, winscard/SCardForgetReader, winscard/SCardForgetReaderA, winscard/SCardForgetReaderW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardForgetReaderW (Unicode) and SCardForgetReaderA (ANSI)
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
 - SCardForgetReaderW
 - winscard/SCardForgetReaderW
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
 - SCardForgetReader
 - SCardForgetReaderA
 - SCardForgetReaderW
---

# SCardForgetReaderW function


## -description

The <b>SCardForgetReader</b> function removes a previously introduced <a href="/windows/desktop/SecGloss/r-gly">reader</a> from control by the <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a>. It is removed from the <a href="/windows/desktop/SecGloss/s-gly">smart card database</a>, including from any <a href="/windows/desktop/SecGloss/r-gly">reader group</a> that it may have been added to.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szReaderName [in]

Display name of the reader to be removed from the smart card database.

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

If the specified reader is the last member of a reader group, the reader group is automatically removed as well.

The <b>SCardForgetReader</b> function is a database management function. For more information on other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.


#### Examples

The following example removes the display name of the specified card reader from the system. The example assumes that lReturn is a valid variable of type <b>LONG</b> and that hContext is a valid handle received from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function.


```cpp

lReturn = SCardForgetReader(hContext, 
                            TEXT("MyReader"));
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetReader\n");

```






> [!NOTE]
> The winscard.h header defines SCardForgetReader as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetcardtypea">SCardForgetCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetreadergroupa">SCardForgetReaderGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadera">SCardIntroduceReader</a>
