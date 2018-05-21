---
UID: NF:winscard.GetOpenCardNameW
title: GetOpenCardNameW function
author: windows-driver-content
description: The GetOpenCardName function displays the smart card &#0034;select card&#0034; dialog box.
old-location: security\getopencardname.htm
old-project: SecAuthN
ms.assetid: b103cec0-dd28-4f90-864b-5f66d044ec55
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetOpenCardName, GetOpenCardName function [Security], GetOpenCardNameA, GetOpenCardNameW, _smart_getopencardname, security.getopencardname, winscard/GetOpenCardName, winscard/GetOpenCardNameA, winscard/GetOpenCardNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetOpenCardNameW (Unicode) and GetOpenCardNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Scarddlg.dll
api_name:
-	GetOpenCardName
-	GetOpenCardNameA
-	GetOpenCardNameW
product: Windows
targetos: Windows
req.lib: Scarddlg.lib
req.dll: Scarddlg.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetOpenCardNameW function


## -description



			The <b>GetOpenCardName</b> function displays the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> "select card" dialog box. Call the function 
<a href="https://msdn.microsoft.com/68014e9e-0ea3-4032-8db5-c1887a1cc9ad">SCardUIDlgSelectCard</a> instead of <b>GetOpenCardName</b>. The <b>GetOpenCardName</b> function is maintained for backward compatibility with version 1.0 of the Microsoft Smart Card Base Components, but calls to <b>GetOpenCardName</b> are mapped to <b>SCardUIDlgSelectCard</b>.
		


## -parameters




### -param Arg1

TBD




#### - pDlgStruc [in]

A pointer to the 
<a href="https://msdn.microsoft.com/b409a6fc-2cfd-491e-8f4c-f8567df7b08f">OPENCARDNAME</a> structure for the "select card" dialog box.


## -returns



The function returns different values depending on whether it succeeds or fails.
						
						
					

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
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b409a6fc-2cfd-491e-8f4c-f8567df7b08f">OPENCARDNAME</a>
 

 

