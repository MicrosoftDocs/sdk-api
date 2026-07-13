---
UID: NF:winscard.SCardUIDlgSelectCardW
title: SCardUIDlgSelectCardW function (winscard.h)
description: Displays the smart card Select Card dialog box. (Unicode)
helpviewer_keywords: ["SCardUIDlgSelectCard", "SCardUIDlgSelectCard function [Security]", "SCardUIDlgSelectCardW", "_smart_scarduidlgselectcard", "security.scarduidlgselectcard", "winscard/SCardUIDlgSelectCard", "winscard/SCardUIDlgSelectCardW"]
old-location: security\scarduidlgselectcard.htm
tech.root: security
ms.assetid: 68014e9e-0ea3-4032-8db5-c1887a1cc9ad
ms.date: 12/05/2018
ms.keywords: SCardUIDlgSelectCard, SCardUIDlgSelectCard function [Security], SCardUIDlgSelectCardA, SCardUIDlgSelectCardW, _smart_scarduidlgselectcard, security.scarduidlgselectcard, winscard/SCardUIDlgSelectCard, winscard/SCardUIDlgSelectCardA, winscard/SCardUIDlgSelectCardW
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardUIDlgSelectCardW (Unicode) and SCardUIDlgSelectCardA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Scarddlg.lib
req.dll: Scarddlg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardUIDlgSelectCardW
 - winscard/SCardUIDlgSelectCardW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Scarddlg.dll
api_name:
 - SCardUIDlgSelectCard
 - SCardUIDlgSelectCardA
 - SCardUIDlgSelectCardW
---

# SCardUIDlgSelectCardW function


## -description

The <b>SCardUIDlgSelectCard</b> function displays the <a href="/windows/desktop/SecGloss/s-gly">smart card</a><b> Select Card</b> dialog box.

## -parameters

### -param unnamedParam1 [in]

Pointer to the 
<a href="/windows/desktop/api/winscard/ns-winscard-opencardname_exa">OPENCARDNAME_EX</a> structure for the <b>Select Card</b> dialog box.

## -returns

If the function successfully displays the 
						<b>Select Card</b> dialog box, the return value is SCARD_S_SUCCESS.

If the function fails, it returns an error code. For more information, see 
<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

## -remarks

The <b>SCardUIDlgSelectCard</b> function provides a method for connecting to a specific <a href="/windows/desktop/SecGloss/s-gly">smart card</a>. When called, this function performs a search for appropriate smart cards matching the <a href="/windows/desktop/api/winscard/ns-winscard-opencard_search_criteriaa">OPENCARD_SEARCH_CRITERIA</a> member specified by the <i>pDlgStruc</i> parameter. Depending on the <b>dwFlags</b> member of <b>pDlgStruc</b>, this function takes the following actions.

<table>
<tr>
<th>Value</th>
<th>Action</th>
</tr>
<tr>
<td>
SC_DLG_FORCE_UI

</td>
<td>
Connects to the card selected by the user from the smart card <b>Select Card</b> dialog box.

</td>
</tr>
<tr>
<td>
SC_DLG_MINIMAL_UI

</td>
<td>
Selects the smart card if only one smart card meets the criteria, or returns information about the user's selection if more than one smart card meets the criteria.

</td>
</tr>
<tr>
<td>
SC_DLG_NO_UI

</td>
<td>
Selects the first available card.

</td>
</tr>
</table>
 

This function replaces 
<a href="/windows/desktop/api/winscard/nf-winscard-getopencardnamea">GetOpenCardName</a>. The <b>GetOpenCardName</b> function is maintained for backward compatibility with version 1.0 of the Microsoft Smart Card Base Components.


#### Examples

The following example  shows how to display the smart card <b>Select Card</b> dialog box.


```cpp
SCARDCONTEXT     hSC;
OPENCARDNAME_EX  dlgStruct;
WCHAR            szReader[256];
WCHAR            szCard[256];
LONG             lReturn;

// Establish a context.
// It will be assigned to the structure's hSCardContext field.
lReturn = SCardEstablishContext(SCARD_SCOPE_USER,
                                NULL,
                                NULL,
                                &hSC );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardEstablishContext\n");
    exit(1);
}

// Initialize the structure.
memset(&dlgStruct, 0, sizeof(dlgStruct));
dlgStruct.dwStructSize = sizeof(dlgStruct);
dlgStruct.hSCardContext = hSC;
dlgStruct.dwFlags = SC_DLG_FORCE_UI;
dlgStruct.lpstrRdr = (LPSTR) szReader;
dlgStruct.nMaxRdr = 256;
dlgStruct.lpstrCard = (LPSTR) szCard;
dlgStruct.nMaxCard = 256;
dlgStruct.lpstrTitle = (LPSTR) "My Select Card Title";

// Display the select card dialog box.
lReturn = SCardUIDlgSelectCard(&dlgStruct);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardUIDlgSelectCard - %x\n", lReturn );
else
    printf("Reader: %S\nCard: %S\n", szReader, szCard );

// Release the context (by SCardReleaseContext - not shown here).

```






> [!NOTE]
> The winscard.h header defines SCardUIDlgSelectCard as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winscard/ns-winscard-opencardname_exa">OPENCARDNAME_EX</a>
