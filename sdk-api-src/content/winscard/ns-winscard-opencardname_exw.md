---
UID: NS:winscard.OPENCARDNAME_EXW
title: OPENCARDNAME_EXW (winscard.h)
description: The OPENCARDNAME_EX structure contains the information that the SCardUIDlgSelectCard function uses to initialize a smart card Select Card dialog box. (Unicode)
helpviewer_keywords: ["*LPOPENCARDNAME_EXW","*POPENCARDNAME_EXW","LPOPENCARDNAME_EX","LPOPENCARDNAME_EX structure pointer [Security]","OPENCARDNAME_EX","OPENCARDNAME_EX structure [Security]","OPENCARDNAME_EXA","OPENCARDNAME_EXW","POPENCARDNAME_EX","POPENCARDNAME_EX structure pointer [Security]","SC_DLG_FORCE_UI","SC_DLG_MINIMAL_UI","SC_DLG_NO_UI","_smart_opencardname_ex","security.opencardname_ex","winscard/LPOPENCARDNAME_EX","winscard/OPENCARDNAME_EX","winscard/OPENCARDNAME_EXA","winscard/OPENCARDNAME_EXW","winscard/POPENCARDNAME_EX"]
old-location: security\opencardname_ex.htm
tech.root: security
ms.assetid: fb9e64a9-441a-4c7b-b404-79682778c694
ms.date: 12/05/2018
ms.keywords: '*LPOPENCARDNAME_EXW, *POPENCARDNAME_EXW, LPOPENCARDNAME_EX, LPOPENCARDNAME_EX structure pointer [Security], OPENCARDNAME_EX, OPENCARDNAME_EX structure [Security], OPENCARDNAME_EXA, OPENCARDNAME_EXW, POPENCARDNAME_EX, POPENCARDNAME_EX structure pointer [Security], SC_DLG_FORCE_UI, SC_DLG_MINIMAL_UI, SC_DLG_NO_UI, _smart_opencardname_ex, security.opencardname_ex, winscard/LPOPENCARDNAME_EX, winscard/OPENCARDNAME_EX, winscard/OPENCARDNAME_EXA, winscard/OPENCARDNAME_EXW, winscard/POPENCARDNAME_EX'
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPENCARDNAME_EXW (Unicode) and OPENCARDNAME_EXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPENCARDNAME_EXW, *POPENCARDNAME_EXW, *LPOPENCARDNAME_EXW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POPENCARDNAME_EXW
 - winscard/POPENCARDNAME_EXW
 - OPENCARDNAME_EXW
 - winscard/OPENCARDNAME_EXW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - OPENCARDNAME_EX
 - OPENCARDNAME_EXA
 - OPENCARDNAME_EXW
---

# OPENCARDNAME_EXW structure


## -description

The <b>OPENCARDNAME_EX</b> structure contains the information that the 
<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a> function uses to initialize a smart card <b>Select Card</b> dialog box.

## -struct-fields

### -field dwStructSize

The length, in bytes, of the structure. The value of this member must not be <b>NULL</b>.

### -field hSCardContext

The context used for communication with the <a href="/windows/desktop/SecGloss/s-gly">smart card</a> <a href="/windows/desktop/SecGloss/r-gly">resource manager</a>. Call 
<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> to set the <a href="/windows/desktop/SecGloss/r-gly">resource manager context</a> and 
<a href="/windows/desktop/api/winscard/nf-winscard-scardreleasecontext">SCardReleaseContext</a> to release it. The value of this member must not be <b>NULL</b>.

### -field hwndOwner

The window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> for the desktop default.

### -field dwFlags

A set of bit flags that you can use to initialize the dialog box. When the dialog box returns, it sets these flags to indicate the user's input. This member can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SC_DLG_MINIMAL_UI"></a><a id="sc_dlg_minimal_ui"></a><dl>
<dt><b>SC_DLG_MINIMAL_UI</b></dt>
</dl>
</td>
<td width="60%">
Display the dialog box only if the card being searched for by the calling application is not located and available for use in a reader. This allows the card to be found, connected (either through the internal dialog box mechanism or the user callback functions), and returned to the calling application.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_DLG_NO_UI"></a><a id="sc_dlg_no_ui"></a><dl>
<dt><b>SC_DLG_NO_UI</b></dt>
</dl>
</td>
<td width="60%">
Force no display of the <b>Select Card</b> <a href="/windows/desktop/SecGloss/u-gly">user interface</a> (UI), regardless of search outcome.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_DLG_FORCE_UI"></a><a id="sc_dlg_force_ui"></a><dl>
<dt><b>SC_DLG_FORCE_UI</b></dt>
</dl>
</td>
<td width="60%">
Force display of the <b>Select Card</b> UI, regardless of the search outcome.

</td>
</tr>
</table>

### -field lpstrTitle

A pointer to a string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the system uses the default title "Select Card:".

### -field lpstrSearchDesc

A pointer to a string to be displayed to the user as a prompt to insert the <a href="/windows/desktop/SecGloss/s-gly">smart card</a>. If this member is <b>NULL</b>, the system uses the default text "Please insert a smart card".

### -field hIcon

A handle to an icon (32 x 32 pixels). You can specify a vendor-specific icon to display in the dialog box. If this value is <b>NULL</b>, a generic, smart card reader–loaded icon is displayed.

### -field pOpenCardSearchCriteria

A pointer to the 
<a href="/windows/desktop/api/winscard/ns-winscard-opencard_search_criteriaa">OPENCARD_SEARCH_CRITERIA</a> structure to be used, or <b>NULL</b>, if one is not used.

### -field lpfnConnect

A pointer to the caller's card connect routine. If the caller needs to perform additional processing to connect to the card, this function pointer is set to the user's connect function. If the connect function is successful, the card is left connected and initialized, and the card handle is returned. 




The prototype for the connect routine is as follows.


```cpp
Connect(
  hSCardContext,  // the card context passed in the parameter block
  szReader,       // the name of the reader
  mszCards,       // multiple string that contains the possible 
                  //  card names in the reader
  pvUserData      // pointer to user data passed in parameter block
);

```

### -field pvUserData

A void pointer to user data. This pointer is passed back to the caller on the Connect routine.

### -field dwShareMode

If <b>lpfnConnect</b> is not <b>NULL</b>, the <b>dwShareMode</b> and <b>dwPreferredProtocols</b> members are ignored. If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is nonzero, an internal call is made to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> that uses <b>dwShareMode</b> and <b>dwPreferredProtocols</b> as the <i>dwShareMode</i> and <i>dwPreferredProtocols</i> parameters. If the connect succeeds, <b>hCardHandle</b> is set to the handle returned by <b>SCardConnect</b>. If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is zero, <b>hCardHandle</b> is set to <b>NULL</b>.

### -field dwPreferredProtocols

Used for internal connection as described in <b>dwShareMode</b>.

### -field lpstrRdr

If the card is located, the <b>lpstrRdr</b> buffer contains the name of the reader that contains the located card. The buffer should be at least 256 characters long.

### -field nMaxRdr

Size, in bytes (ANSI version) or characters (<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> version), of the buffer pointed to by <b>lpstrRdr</b>. If the buffer is too small to contain the reader information, 
<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a> returns SCARD_E_NO_MEMORY and the required size of the buffer pointed to by <b>lpstrRdr</b>.

### -field lpstrCard

If the card is located, the <i>lpstrCard</i> buffer contains the name of the located card. The buffer should be at least 256 characters long.

### -field nMaxCard

Size, in bytes (ANSI version) or characters (<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> version), of the buffer pointed to by <i>lpstrCard</i>. If the buffer is too small to contain the card information, 
<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a> returns SCARD_E_NO_MEMORY and the required size of the buffer in <b>nMaxCard</b>.

### -field dwActiveProtocol

The actual protocol in use when the dialog box makes a connection to a card.

### -field hCardHandle

A handle of the connected card (either through an internal dialog box connect or an <b>lpfnConnect</b> callback).

## -see-also

<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scardreleasecontext">SCardReleaseContext</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a>



<a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>

## -remarks

> [!NOTE]
> The winscard.h header defines OPENCARDNAME_EX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

