---
UID: NF:winscard.SCardEndTransaction
title: SCardEndTransaction function
author: windows-driver-content
description: Completes a previously declared transaction, allowing other applications to resume interactions with the card.
old-location: security\scardendtransaction.htm
old-project: SecAuthN
ms.assetid: 0acaff20-006a-47d3-bc7a-834b3281cde6
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: SCARD_EJECT_CARD, SCARD_LEAVE_CARD, SCARD_RESET_CARD, SCARD_UNPOWER_CARD, SCardEndTransaction, SCardEndTransaction function [Security], _smart_scardendtransaction, security.scardendtransaction, winscard/SCardEndTransaction
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
req.unicode-ansi: 
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
-	Winscard.dll
-	Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
-	SCardEndTransaction
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardEndTransaction function


## -description


The <b>SCardEndTransaction</b> function completes a previously declared <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">transaction</a>, allowing other applications to resume interactions with the card.


## -parameters




### -param hCard [in]

Reference value obtained from a previous call to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>. This value would also have been used in an earlier call to 
<a href="https://msdn.microsoft.com/91f61060-4b0b-4890-9372-25ba0aacb642">SCardBeginTransaction</a>.


### -param dwDisposition [in]

Action to take on the card in the connected reader on close. 
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_EJECT_CARD"></a><a id="scard_eject_card"></a><dl>
<dt><b>SCARD_EJECT_CARD</b></dt>
</dl>
</td>
<td width="60%">
Eject the card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_LEAVE_CARD"></a><a id="scard_leave_card"></a><dl>
<dt><b>SCARD_LEAVE_CARD</b></dt>
</dl>
</td>
<td width="60%">
Do not do anything special.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_RESET_CARD"></a><a id="scard_reset_card"></a><dl>
<dt><b>SCARD_RESET_CARD</b></dt>
</dl>
</td>
<td width="60%">
Reset the card.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_UNPOWER_CARD"></a><a id="scard_unpower_card"></a><dl>
<dt><b>SCARD_UNPOWER_CARD</b></dt>
</dl>
</td>
<td width="60%">
Power down the card.

</td>
</tr>
</table>
 


## -returns




					If the function succeeds, the function returns <b>SCARD_S_SUCCESS</b>. 

If the function fails, it returns an error code. For more information, see <a href="authentication_return_values.htm">Smart Card Return Values</a>.   Possible error codes follow.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_W_RESET_CARD</b></dt>
<dt>0x80100068L</dt>
</dl>
</td>
<td width="60%">
The transaction was released. Any future communication with the card requires a call to the <a href="https://msdn.microsoft.com/c79e5810-c2be-4184-8ac7-c058ccb9308e">SCardReconnect</a> function.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>The transaction was not released. The application must immediately call the <a href="https://msdn.microsoft.com/d087a006-bd2d-4ad7-965b-36ea8d712ec8">SCardDisconnect</a>, <a href="https://msdn.microsoft.com/c79e5810-c2be-4184-8ac7-c058ccb9308e">SCardReconnect</a>, or <a href="https://msdn.microsoft.com/aa17cf94-ca66-4b5e-b1cd-00319f496b09">SCardReleaseContext</a> function to avoid an existing transaction blocking other threads and processes from communicating with the smart card.

</td>
</tr>
</table>
 




## -remarks



The <b>SCardEndTransaction</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> and <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> access function. For more information on other access functions, see 
<a href="https://msdn.microsoft.com/37d92491-174b-471e-b36e-46d9285dd404">Smart Card and Reader Access Functions</a>.


#### Examples

The following example ends a smart card transaction. The example assumes that lReturn is a valid variable of type <b>LONG</b>, that hCard is a valid handle received from a previous call to the <a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a> function, and that hCard was passed to a previous call to the <a href="https://msdn.microsoft.com/91f61060-4b0b-4890-9372-25ba0aacb642">SCardBeginTransaction</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardEndTransaction(hCard, 
                              SCARD_LEAVE_CARD);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardEndTransaction\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/91f61060-4b0b-4890-9372-25ba0aacb642">SCardBeginTransaction</a>



<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>
 

 

