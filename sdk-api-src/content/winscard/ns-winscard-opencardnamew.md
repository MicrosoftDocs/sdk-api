---
UID: NS:winscard.OPENCARDNAMEW
title: OPENCARDNAMEW
author: windows-sdk-content
description: Contains the information that the GetOpenCardName function uses to initialize a smart card Select Card dialog box.
old-location: security\opencardname.htm
old-project: SecAuthN
ms.assetid: b409a6fc-2cfd-491e-8f4c-f8567df7b08f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*LPOPENCARDNAMEW, *POPENCARDNAMEW, LPOPENCARDNAME, LPOPENCARDNAME structure pointer [Security], OPENCARDNAME, OPENCARDNAME structure [Security], OPENCARDNAMEA, OPENCARDNAMEW, SC_DLG_FORCE_UI, SC_DLG_MINIMAL_UI, SC_DLG_NO_UI, _smart_opencardname, security.opencardname, winscard/LPOPENCARDNAME, winscard/OPENCARDNAME, winscard/OPENCARDNAMEA, winscard/OPENCARDNAMEW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OPENCARDNAMEW (Unicode) and OPENCARDNAMEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: OPENCARDNAMEW, *POPENCARDNAMEW, *LPOPENCARDNAMEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - OPENCARDNAME
 - OPENCARDNAMEA
 - OPENCARDNAMEW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OPENCARDNAMEW structure


## -description


The <b>OPENCARDNAME</b> structure contains the information that the 
<a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a> function uses to initialize a smart card <b>Select Card</b> dialog box. Calling <a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> with <a href="https://msdn.microsoft.com/fb9e64a9-441a-4c7b-b404-79682778c694">OPENCARDNAME_EX</a> is recommended over calling <a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a> with <b>OPENCARDNAME</b>. <b>OPENCARDNAME</b> is provided for backward compatibility.


## -struct-fields




### -field dwStructSize

Specifies the length, in bytes, of the structure. This member must not be <b>NULL</b>.


### -field hwndOwner

The window that owns the dialog box. This member can be any valid window handle, or it can be <b>NULL</b> for desktop default.


### -field hSCardContext

The context used for communication with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a>. Call 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> to set the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> and 
<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a> to release it. This member must not be <b>NULL</b>.


### -field lpstrGroupNames

A pointer to a buffer that contains null-terminated group name strings. The last string in the buffer must be terminated by two null characters. Each string is the name of a group of cards that is to be included in the search. If <b>lpstrGroupNames</b> is <b>NULL</b>, the default group (<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Scard$DefaultReaders</a>) is searched.


### -field nMaxGroupNames

The maximum number of bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version) in the <b>lpstrGroupNames</b> string.


### -field lpstrCardNames

A pointer to a buffer that contains null-terminated card name strings. The last string in the buffer must be terminated by two null characters. Each string is the name of a card that is to be located.


### -field nMaxCardNames

The maximum number of bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version) in the <b>lpstrCardNames</b> string.


### -field rgguidInterfaces

Reserved for future use. Set to <b>NULL</b>. An array of GUIDs that identify the interfaces required.


### -field cguidInterfaces

Reserved for futures use. Set to <b>NULL</b>. The number of interfaces in the <b>rgguidInterfaces</b> array.


### -field lpstrRdr

If the card is located, the <b>lpstrRdr</b> buffer contains the name of the reader that contains the located card. The buffer should be at least 256 characters long.


### -field nMaxRdr

The size, in bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version), of the buffer pointed to by <b>lpstrRdr</b>. If the buffer is too small to contain the reader information, 
<a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a> returns SCARD_E_NO_MEMORY and the required size of the buffer pointed to by <b>lpstrRdr</b>.


### -field lpstrCard

If the card is located, the <b>lpstrCard</b> buffer contains the name of the located card. The buffer should be at least 256 characters long.


### -field nMaxCard

The size, in bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version), of the buffer pointed to by <b>lpstrCard</b>. If the buffer is too small to contain the card information, <a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a> returns SCARD_E_NO_MEMORY and the required size of the buffer in <b>nMaxCard</b>.


### -field lpstrTitle

 A pointer to a string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the system uses the default title "Select Card:".


### -field dwFlags

A set of bit flags you can use to initialize the dialog box. When the dialog box returns, it sets these flags to indicate the input of the user. This member can be a combination of the following flags.

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
Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader. This allows the card to be found, connected (either through the internal dialog box mechanism or the user callback functions), and returned to the calling application.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_DLG_NO_UI"></a><a id="sc_dlg_no_ui"></a><dl>
<dt><b>SC_DLG_NO_UI</b></dt>
</dl>
</td>
<td width="60%">
Force no display of the <b>Select Card</b> <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">user interface</a> (UI), regardless of search outcome.

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
 


### -field pvUserData

A void pointer to user data. This pointer is passed back to the caller on the Connect, Check, and Disconnect routines.


### -field dwShareMode

If <b>lpfnConnect</b> is not <b>NULL</b>, the <b>dwShareMode</b> and <b>dwPreferredProtocols</b> members are ignored.

If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is nonzero, then an internal call is made to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> that uses <b>dwShareMode</b> and <b>dwPreferredProtocols</b> as the <i>dwShareMode</i> and <i>dwPreferredProtocols</i> parameters. If the connect succeeds, <b>hCardHandle</b> is set to the handle returned by <b>hSCardConnect</b>. 

If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is zero, the dialog box returns <b>hCardHandle</b> as <b>NULL</b>.


### -field dwPreferredProtocols

Used for internal connection as described in <b>dwShareMode</b>.


### -field dwActiveProtocol

Returns the actual protocol in use when the dialog box makes a connection to a card.


### -field lpfnConnect

A pointer to the card connect routine of the caller. If the caller needs to perform additional processing to connect to the card, this function pointer is set to the connect function for the user. If the connect function is successful, the card is left connected and initialized, and the card handle is returned. 




The prototype for the connect routine is as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Connect(
  hSCardContext, // the card context passed in the parameter block
  szReader,      // the name of the reader
  mszCards,      // multiple string that contains the 
                 //    possible card names in the reader
  pvUserData     // pointer to user data passed in parameter block
);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnCheck

A pointer to the card verify routine of the caller. If no special card verification is required, this pointer is <b>NULL</b>. 




If the card is rejected by the verify routine, <b>FALSE</b> is returned and the card is disconnected, as indicated by <b>lpfnDisconnect</b>.

If the card is accepted by the verify routine, <b>TRUE</b> is returned. When the user accepts the card, all other cards currently connected will be disconnected, as indicated by <b>lpfnDisconnect</b>, and this card will be returned as the located card. The located card will remain connected.

The prototype for the check routine is as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Check(
  hSCardContext, // the card context passed in the parameter block
  hCard,         // card handle
  pvUserData     // pointer to user data passed in the parameter block
);
</pre>
</td>
</tr>
</table></span></div>

### -field lpfnDisconnect

A pointer to the card disconnect routine of the caller. 




The prototype for the disconnect routine is as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Disconnect(
  hSCardContext, // the card context passed in the parameter block
  hCard,         // card handle
  pvUserData     // pointer to user data passed in the parameter block
);
</pre>
</td>
</tr>
</table></span></div>
<div class="alert"><b>Note</b>  When using <b>lpfnConnect</b>, <b>lpfnCheck</b>, and <b>lpfnDisconnect</b>, all three callback procedures should be present. Using these callbacks allows further verification that the calling application has found the appropriate card. This is the best way to ensure the appropriate card is selected.</div>
<div> </div>

### -field hCardHandle

A handle of the connected card (either through an internal dialog box connect or an <b>lpfnConnect</b> callback).


## -see-also




<a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a>



<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a>



<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a>
 

 

