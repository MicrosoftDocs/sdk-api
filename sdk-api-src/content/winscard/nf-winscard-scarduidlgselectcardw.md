---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SCardUIDlgSelectCardW function


## -description


The <b>SCardUIDlgSelectCard</b> function displays the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a><b> Select Card</b> dialog box.


## -parameters




### -param Arg1

TBD




#### - pDlgStruc [in]

Pointer to the 
<a href="https://msdn.microsoft.com/fb9e64a9-441a-4c7b-b404-79682778c694">OPENCARDNAME_EX</a> structure for the <b>Select Card</b> dialog box.


## -returns



If the function successfully displays the 
						<b>Select Card</b> dialog box, the return value is SCARD_S_SUCCESS.

If the function fails, it returns an error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.




## -remarks



The <b>SCardUIDlgSelectCard</b> function provides a method for connecting to a specific <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a>. When called, this function performs a search for appropriate smart cards matching the <a href="https://msdn.microsoft.com/f20874ca-a714-45b7-abcb-85bedc4e6245">OPENCARD_SEARCH_CRITERIA</a> member specified by the <i>pDlgStruc</i> parameter. Depending on the <b>dwFlags</b> member of <b>pDlgStruc</b>, this function takes the following actions.

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
<a href="https://msdn.microsoft.com/b103cec0-dd28-4f90-864b-5f66d044ec55">GetOpenCardName</a>. The <b>GetOpenCardName</b> function is maintained for backward compatibility with version 1.0 of the Microsoft Smart Card Base Components.


#### Examples

The following example  shows how to display the smart card <b>Select Card</b> dialog box.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SCARDCONTEXT     hSC;
OPENCARDNAME_EX  dlgStruct;
WCHAR            szReader[256];
WCHAR            szCard[256];
LONG             lReturn;

// Establish a context.
// It will be assigned to the structure's hSCardContext field.
lReturn = SCardEstablishContext(SCARD_SCOPE_USER,
                                NULL,
                                NULL,
                                &amp;hSC );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardEstablishContext\n");
    exit(1);
}

// Initialize the structure.
memset(&amp;dlgStruct, 0, sizeof(dlgStruct));
dlgStruct.dwStructSize = sizeof(dlgStruct);
dlgStruct.hSCardContext = hSC;
dlgStruct.dwFlags = SC_DLG_FORCE_UI;
dlgStruct.lpstrRdr = (LPSTR) szReader;
dlgStruct.nMaxRdr = 256;
dlgStruct.lpstrCard = (LPSTR) szCard;
dlgStruct.nMaxCard = 256;
dlgStruct.lpstrTitle = (LPSTR) "My Select Card Title";

// Display the select card dialog box.
lReturn = SCardUIDlgSelectCard(&amp;dlgStruct);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardUIDlgSelectCard - %x\n", lReturn );
else
    printf("Reader: %S\nCard: %S\n", szReader, szCard );

// Release the context (by SCardReleaseContext - not shown here).
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fb9e64a9-441a-4c7b-b404-79682778c694">OPENCARDNAME_EX</a>
 

 

