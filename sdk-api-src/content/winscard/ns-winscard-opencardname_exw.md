---
UID: NS:winscard.OPENCARDNAME_EXW
title: OPENCARDNAME_EXW
author: windows-sdk-content
description: The OPENCARDNAME_EX structure contains the information that the SCardUIDlgSelectCard function uses to initialize a smart card Select Card dialog box.
old-location: security\opencardname_ex.htm
tech.root: secauthn
ms.assetid: fb9e64a9-441a-4c7b-b404-79682778c694
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*LPOPENCARDNAME_EXW, *POPENCARDNAME_EXW, LPOPENCARDNAME_EX, LPOPENCARDNAME_EX structure pointer [Security], OPENCARDNAME_EX, OPENCARDNAME_EX structure [Security], OPENCARDNAME_EXA, OPENCARDNAME_EXW, POPENCARDNAME_EX, POPENCARDNAME_EX structure pointer [Security], SC_DLG_FORCE_UI, SC_DLG_MINIMAL_UI, SC_DLG_NO_UI, _smart_opencardname_ex, security.opencardname_ex, winscard/LPOPENCARDNAME_EX, winscard/OPENCARDNAME_EX, winscard/OPENCARDNAME_EXA, winscard/OPENCARDNAME_EXW, winscard/POPENCARDNAME_EX"
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
req.unicode-ansi: OPENCARDNAME_EXW (Unicode) and OPENCARDNAME_EXA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: OPENCARDNAME_EXW, *POPENCARDNAME_EXW, *LPOPENCARDNAME_EXW
req.redist: 
---

# OPENCARDNAME_EXW structure


## -description


The <b>OPENCARDNAME_EX</b> structure contains the information that the 
<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> function uses to initialize a smart card <b>Select Card</b> dialog box.


## -struct-fields




### -field dwStructSize

The length, in bytes, of the structure. The value of this member must not be <b>NULL</b>.


### -field hSCardContext

The context used for communication with the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a>. Call 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> to set the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> and 
<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a> to release it. The value of this member must not be <b>NULL</b>.


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
 


### -field lpstrTitle

A pointer to a string to be placed in the title bar of the dialog box. If this member is <b>NULL</b>, the system uses the default title "Select Card:".


### -field lpstrSearchDesc

A pointer to a string to be displayed to the user as a prompt to insert the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a>. If this member is <b>NULL</b>, the system uses the default text "Please insert a smart card".


### -field hIcon

A handle to an icon (32 x 32 pixels). You can specify a vendor-specific icon to display in the dialog box. If this value is <b>NULL</b>, a generic, smart card reader–loaded icon is displayed.


### -field pOpenCardSearchCriteria

A pointer to the 
<a href="https://msdn.microsoft.com/f20874ca-a714-45b7-abcb-85bedc4e6245">OPENCARD_SEARCH_CRITERIA</a> structure to be used, or <b>NULL</b>, if one is not used.


### -field lpfnConnect

A pointer to the caller's card connect routine. If the caller needs to perform additional processing to connect to the card, this function pointer is set to the user's connect function. If the connect function is successful, the card is left connected and initialized, and the card handle is returned. 




The prototype for the connect routine is as follows.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>Connect(
  hSCardContext,  // the card context passed in the parameter block
  szReader,       // the name of the reader
  mszCards,       // multiple string that contains the possible 
                  //  card names in the reader
  pvUserData      // pointer to user data passed in parameter block
);
</pre>
</td>
</tr>
</table></span></div>

### -field pvUserData

A void pointer to user data. This pointer is passed back to the caller on the Connect routine.


### -field dwShareMode

If <b>lpfnConnect</b> is not <b>NULL</b>, the <b>dwShareMode</b> and <b>dwPreferredProtocols</b> members are ignored. If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is nonzero, an internal call is made to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> that uses <b>dwShareMode</b> and <b>dwPreferredProtocols</b> as the <i>dwShareMode</i> and <i>dwPreferredProtocols</i> parameters. If the connect succeeds, <b>hCardHandle</b> is set to the handle returned by <b>SCardConnect</b>. If <b>lpfnConnect</b> is <b>NULL</b> and <b>dwShareMode</b> is zero, <b>hCardHandle</b> is set to <b>NULL</b>.


### -field dwPreferredProtocols

Used for internal connection as described in <b>dwShareMode</b>.


### -field lpstrRdr

If the card is located, the <b>lpstrRdr</b> buffer contains the name of the reader that contains the located card. The buffer should be at least 256 characters long.


### -field nMaxRdr

Size, in bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version), of the buffer pointed to by <b>lpstrRdr</b>. If the buffer is too small to contain the reader information, 
<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> returns SCARD_E_NO_MEMORY and the required size of the buffer pointed to by <b>lpstrRdr</b>.


### -field lpstrCard

If the card is located, the <i>lpstrCard</i> buffer contains the name of the located card. The buffer should be at least 256 characters long.


### -field nMaxCard

Size, in bytes (ANSI version) or characters (<a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version), of the buffer pointed to by <i>lpstrCard</i>. If the buffer is too small to contain the card information, 
<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> returns SCARD_E_NO_MEMORY and the required size of the buffer in <b>nMaxCard</b>.


### -field dwActiveProtocol

The actual protocol in use when the dialog box makes a connection to a card.


### -field hCardHandle

A handle of the connected card (either through an internal dialog box connect or an <b>lpfnConnect</b> callback).


## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a>



<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a>



<a href="authentication_return_values.htm">Smart Card Return Values</a>
 

 

