---
UID: NS:winscard.OPENCARD_SEARCH_CRITERIAA
title: OPENCARD_SEARCH_CRITERIAA (winscard.h)
description: The OPENCARD_SEARCH_CRITERIA structure is used by the SCardUIDlgSelectCard function in order to recognize cards that meet the requirements set forth by the caller. You can, however, call SCardUIDlgSelectCard without using this structure. (ANSI)
helpviewer_keywords: ["*LPOPENCARD_SEARCH_CRITERIAA","*POPENCARD_SEARCH_CRITERIAA","LPOPENCARD_SEARCH_CRITERIA","LPOPENCARD_SEARCH_CRITERIA structure pointer [Security]","OPENCARD_SEARCH_CRITERIA","OPENCARD_SEARCH_CRITERIA structure [Security]","OPENCARD_SEARCH_CRITERIAA","OPENCARD_SEARCH_CRITERIAW","POPENCARD_SEARCH_CRITERIA","POPENCARD_SEARCH_CRITERIA structure pointer [Security]","_smart_opencard_search_criteria","security.opencard_search_criteria","winscard/LPOPENCARD_SEARCH_CRITERIA","winscard/OPENCARD_SEARCH_CRITERIA","winscard/OPENCARD_SEARCH_CRITERIAA","winscard/OPENCARD_SEARCH_CRITERIAW","winscard/POPENCARD_SEARCH_CRITERIA"]
old-location: security\opencard_search_criteria.htm
tech.root: security
ms.assetid: f20874ca-a714-45b7-abcb-85bedc4e6245
ms.date: 12/05/2018
ms.keywords: '*LPOPENCARD_SEARCH_CRITERIAA, *POPENCARD_SEARCH_CRITERIAA, LPOPENCARD_SEARCH_CRITERIA, LPOPENCARD_SEARCH_CRITERIA structure pointer [Security], OPENCARD_SEARCH_CRITERIA, OPENCARD_SEARCH_CRITERIA structure [Security], OPENCARD_SEARCH_CRITERIAA, OPENCARD_SEARCH_CRITERIAW, POPENCARD_SEARCH_CRITERIA, POPENCARD_SEARCH_CRITERIA structure pointer [Security], _smart_opencard_search_criteria, security.opencard_search_criteria, winscard/LPOPENCARD_SEARCH_CRITERIA, winscard/OPENCARD_SEARCH_CRITERIA, winscard/OPENCARD_SEARCH_CRITERIAA, winscard/OPENCARD_SEARCH_CRITERIAW, winscard/POPENCARD_SEARCH_CRITERIA'
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPENCARD_SEARCH_CRITERIAW (Unicode) and OPENCARD_SEARCH_CRITERIAA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPENCARD_SEARCH_CRITERIAA, *POPENCARD_SEARCH_CRITERIAA, *LPOPENCARD_SEARCH_CRITERIAA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - POPENCARD_SEARCH_CRITERIAA
 - winscard/POPENCARD_SEARCH_CRITERIAA
 - OPENCARD_SEARCH_CRITERIAA
 - winscard/OPENCARD_SEARCH_CRITERIAA
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
 - OPENCARD_SEARCH_CRITERIA
 - OPENCARD_SEARCH_CRITERIAA
 - OPENCARD_SEARCH_CRITERIAW
---

# OPENCARD_SEARCH_CRITERIAA structure


## -description

The <b>OPENCARD_SEARCH_CRITERIA</b> structure is used by the 
<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a> function in order to recognize cards that meet the requirements set forth by the caller. You can, however, call <b>SCardUIDlgSelectCard</b> without using this structure.

## -struct-fields

### -field dwStructSize

The length, in bytes, of the structure. Must not be <b>NULL</b>.

### -field lpstrGroupNames

A pointer to a buffer containing null-terminated group name strings. The last string in the buffer must be terminated by two null characters. Each string is the name of a group of cards that is to be included in the search. If <b>lpstrGroupNames</b> is <b>NULL</b>, the default group (<a href="/windows/desktop/SecGloss/s-gly">Scard$DefaultReaders</a>) is searched.

### -field nMaxGroupNames

The maximum number of bytes (ANSI version) or characters (<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> version) in the <b>lpstrGroupNames</b> string.

### -field rgguidInterfaces

Reserved for future use. An array of GUIDs that identifies the interfaces required. Set this member to <b>NULL</b>.

### -field cguidInterfaces

Reserved for future use. The number of interfaces in the <b>rgguidInterfaces</b> array. Set this member to <b>NULL</b>.

### -field lpstrCardNames

A pointer to a buffer that contains null-terminated card name strings. The last string in the buffer must be terminated by two null characters. Each string is the name of a card that is to be located.

### -field nMaxCardNames

The maximum number of bytes (ANSI version) or characters (Unicode version) in the <b>lpstrGroupNames</b> string.

### -field lpfnCheck

A pointer to the caller's card verify routine. If no special card verification is required, this pointer is <b>NULL</b>. If the card is rejected by the verify routine, <b>FALSE</b> is returned, and the card will be disconnected. If the card is accepted by the verify routine, <b>TRUE</b> is returned. 




The prototype for the check routine is as follows.


```cpp
Boolean Check(
  hSCardContext, // the card context passed in the parameter block
  hCard,         // card handle
  pvUserData     // pointer to user data passed in the parameter block
);

```

### -field lpfnConnect

A pointer to the caller's card connect routine. If the caller needs to perform additional processing to connect to the card, this function pointer is set to the user's connect function. If the connect function is successful, the card is left connected and initialized, and the card handle is returned. 




The prototype for the connect routine is as follows.


```cpp
Connect(
  hSCardContext, // the card context passed in the parameter block
  szReader,      // the name of the reader
  mszCards,      // multiple string that contains
                 //    the possible card names in the reader
  pvUserData     // pointer to user data passed in parameter block
);

```

### -field lpfnDisconnect

A pointer to the caller's card disconnect routine. 




The prototype for the disconnect routine is as follows.


```cpp
Disconnect(
  hSCardContext, // the card context passed in the parameter block
  hCard,         // card handle
  pvUserData     // pointer to user data passed in the parameter block
);

```


<div class="alert"><b>Note</b>  When you use <b>lpfnConnect</b>, <b>lpfnCheck</b>, and <b>lpfnDisconnect</b>, all three callback procedures should be present. Using these callbacks allows further verification that the calling application has found the appropriate card. This is the best way to ensure the appropriate card is selected. However, when using a value that is not <b>NULL</b> for <b>lpfnCheck</b>, either both <b>lpfnConnect</b> and <b>lpfnDisconnect</b> must not be <b>NULL</b> (and <b>pvUserData</b> should also be provided), or <b>dwShareMode</b> and <b>dwPreferredProtocols</b> must both be set.</div>
<div> </div>

### -field pvUserData

Void pointer to user data. This pointer is passed back to the caller on the Connect, Check, and Disconnect routines.

### -field dwShareMode

If <b>lpfnConnect</b> is not <b>NULL</b>, the <b>dwShareMode</b> and <b>dwPreferredProtocols</b> members are ignored. If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is nonzero, an internal call is made to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a> that uses <b>dwShareMode</b> and <b>dwPreferredProtocols</b> as the parameter.

### -field dwPreferredProtocols

Used for internal connection as described in <b>dwShareMode</b>.

## -see-also

<a href="/windows/desktop/api/winscard/ns-winscard-opencardname_exa">OPENCARDNAME_EX</a>



<a href="/windows/desktop/api/winscard/nf-winscard-scarduidlgselectcarda">SCardUIDlgSelectCard</a>

## -remarks

> [!NOTE]
> The winscard.h header defines OPENCARD_SEARCH_CRITERIA as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

