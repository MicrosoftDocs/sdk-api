---
UID: NF:winscard.SCardIntroduceCardTypeA
title: SCardIntroduceCardTypeA function (winscard.h)
description: Introduces a smart card to the smart card subsystem (for the active user) by adding it to the smart card database. (ANSI)
helpviewer_keywords: ["SCardIntroduceCardTypeA", "winscard/SCardIntroduceCardTypeA"]
old-location: security\scardintroducecardtype.htm
tech.root: security
ms.assetid: 1ac88466-1277-44d7-a471-b31d6bfce99e
ms.date: 12/05/2018
ms.keywords: SCardIntroduceCardType, SCardIntroduceCardType function [Security], SCardIntroduceCardTypeA, SCardIntroduceCardTypeW, _smart_scardintroducecardtype, security.scardintroducecardtype, winscard/SCardIntroduceCardType, winscard/SCardIntroduceCardTypeA, winscard/SCardIntroduceCardTypeW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardIntroduceCardTypeW (Unicode) and SCardIntroduceCardTypeA (ANSI)
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
 - SCardIntroduceCardTypeA
 - winscard/SCardIntroduceCardTypeA
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
 - SCardIntroduceCardType
 - SCardIntroduceCardTypeA
 - SCardIntroduceCardTypeW
---

# SCardIntroduceCardTypeA function


## -description

The <b>SCardIntroduceCardType</b> function introduces a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> to the <a href="/windows/desktop/SecGloss/s-gly">smart card subsystem</a> (for the active user) by adding it to the <a href="/windows/desktop/SecGloss/s-gly">smart card database</a>.

## -parameters

### -param hContext [in]

Handle that identifies the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.

### -param szCardName [in]

Name by which the user can recognize the card.

### -param pguidPrimaryProvider [in, optional]

Pointer to the identifier (GUID) for the smart card's <a href="/windows/desktop/SecGloss/p-gly">primary service provider</a>.

### -param rgguidInterfaces [in, optional]

Array of identifiers (GUIDs) that identify the interfaces supported by the smart card.

### -param dwInterfaceCount [in]

Number of identifiers in the <i>rgguidInterfaces</i> array.

### -param pbAtr [in]

<a href="/windows/desktop/SecGloss/a-gly">ATR string</a> that can be used for matching purposes when querying the smart card database (for more information, see 
<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>). The length of this string is determined by normal ATR parsing.

### -param pbAtrMask [in]

Optional bitmask to use when comparing the ATRs of smart cards to the ATR supplied in <i>pbAtr</i>. If this value is non-<b>NULL</b>, it must point to a string of bytes the same length as the ATR string supplied in <i>pbAtr</i>. When a given ATR string <i>A</i> is compared to the ATR supplied in <i>pbAtr</i>, it matches if and only if <i>A &amp; M</i> = <i>pbAtr</i>, where <i>M</i> is the supplied mask, and <i>&amp;</i> represents bitwise AND.

### -param cbAtrLen [in]

Length of the ATR and optional ATR mask. If this value is zero, then the length of the ATR is determined by normal ATR parsing. This value cannot be zero if a <i>pbAtr</i> value is supplied.

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

This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardIntroduceCardType</b> function is a database management function. For more information on other database management functions, see 
<a href="/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.

To remove a smart card, use 
<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetcardtypea">SCardForgetCardType</a>.


#### Examples

The following example shows how to introduce a card type. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function.


```cpp
GUID  MyGuid = { 0xABCDEF00,
                 0xABCD,
                 0xABCD,
                 0xAA, 0xBB, 0xCC, 0xDD,
                 0xAA, 0xBB, 0xCC, 0xDD };

static const BYTE MyATR[] =     { 0xaa, 0xbb, 0xcc, 0x00, 0xdd };
static const BYTE MyATRMask[] = { 0xff, 0xff, 0xff, 0x00, 0xff};

LONG            lReturn;

lReturn = SCardIntroduceCardType(hContext, 
                                 L"MyCardName",
                                 &MyGuid,
                                 NULL,    // No interface array
                                 0,       // Interface count = 0
                                 MyATR,
                                 MyATRMask,
                                 sizeof(MyATR));
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardIntroduceCardType\n");

```






> [!NOTE]
> The winscard.h header defines SCardIntroduceCardType as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardforgetcardtypea">SCardForgetCardType</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadera">SCardIntroduceReader</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardintroducereadergroupa">SCardIntroduceReaderGroup</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardlistcardsa">SCardListCards</a>
