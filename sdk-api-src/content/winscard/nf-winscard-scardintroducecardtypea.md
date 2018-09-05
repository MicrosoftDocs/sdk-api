---
UID: NF:winscard.SCardIntroduceCardTypeA
title: SCardIntroduceCardTypeA function
author: windows-sdk-content
description: Introduces a smart card to the smart card subsystem (for the active user) by adding it to the smart card database.
old-location: security\scardintroducecardtype.htm
old-project: SecAuthN
ms.assetid: 1ac88466-1277-44d7-a471-b31d6bfce99e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: SCardIntroduceCardType, SCardIntroduceCardType function [Security], SCardIntroduceCardTypeA, SCardIntroduceCardTypeW, _smart_scardintroducecardtype, security.scardintroducecardtype, winscard/SCardIntroduceCardType, winscard/SCardIntroduceCardTypeA, winscard/SCardIntroduceCardTypeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winscard.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
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
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardIntroduceCardTypeA function


## -description


The <b>SCardIntroduceCardType</b> function introduces a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a> (for the active user) by adding it to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card database</a>.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szCardName [in]

Name by which the user can recognize the card.


### -param pguidPrimaryProvider [in, optional]

Pointer to the identifier (GUID) for the smart card's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary service provider</a>.


### -param rgguidInterfaces [in, optional]

Array of identifiers (GUIDs) that identify the interfaces supported by the smart card.


### -param dwInterfaceCount [in]

Number of identifiers in the <i>rgguidInterfaces</i> array.


### -param pbAtr [in]

<a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">ATR string</a> that can be used for matching purposes when querying the smart card database (for more information, see 
<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>). The length of this string is determined by normal ATR parsing.


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
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardIntroduceCardType</b> function is a database management function. For more information on other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.

To remove a smart card, use 
<a href="https://msdn.microsoft.com/4f2d4791-d517-43e4-bff9-f88e12983dea">SCardForgetCardType</a>.


#### Examples

The following example shows how to introduce a card type. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GUID  MyGuid = { 0xABCDEF00,
                 0xABCD,
                 0xABCD,
                 0xAA, 0xBB, 0xCC, 0xDD,
                 0xAA, 0xBB, 0xCC, 0xDD };

static const BYTE MyATR[] =     { 0xaa, 0xbb, 0xcc, 0x00, 0xdd };
static const BYTE MyATRMask[] = { 0xff, 0xff, 0xff, 0x00, 0xff};

LONG            lReturn;

lReturn = SCardIntroduceCardType(hContext, 
                                 L"MyCardName",
                                 &amp;MyGuid,
                                 NULL,    // No interface array
                                 0,       // Interface count = 0
                                 MyATR,
                                 MyATRMask,
                                 sizeof(MyATR));
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardIntroduceCardType\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/4f2d4791-d517-43e4-bff9-f88e12983dea">SCardForgetCardType</a>



<a href="https://msdn.microsoft.com/1f8b9d75-5bba-40c3-99a0-6910855fcd4d">SCardIntroduceReader</a>



<a href="https://msdn.microsoft.com/aaf7d2f9-71d5-42bb-a96f-71124be40aa3">SCardIntroduceReaderGroup</a>



<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>
 

 

