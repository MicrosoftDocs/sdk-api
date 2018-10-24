---
UID: NF:winscard.SCardLocateCardsByATRW
title: SCardLocateCardsByATRW function
author: windows-sdk-content
description: Searches the readers listed in the rgReaderStates parameter for a card with a name that matches one of the card names contained in one of the SCARD_ATRMASK structures specified by the rgAtrMasks parameter.
old-location: security\scardlocatecardsbyatr.htm
tech.root: secauthn
ms.assetid: 6c4a644c-033f-4654-b96d-0379e9ac0bb4
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SCardLocateCardsByATR, SCardLocateCardsByATR function [Security], SCardLocateCardsByATRA, SCardLocateCardsByATRW, _smart_scardlocatecardsbyatr, security.scardlocatecardsbyatr, winscard/SCardLocateCardsByATR, winscard/SCardLocateCardsByATRA, winscard/SCardLocateCardsByATRW
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
req.unicode-ansi: SCardLocateCardsByATRW (Unicode) and SCardLocateCardsByATRA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardLocateCardsByATR
 - SCardLocateCardsByATRA
 - SCardLocateCardsByATRW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardLocateCardsByATRW function


## -description


The <b>SCardLocateCardsByATR</b> function searches the readers listed in the <i>rgReaderStates</i> parameter for a card with a name that matches one of the card names contained in one of the <a href="https://msdn.microsoft.com/d7f1a747-a858-4bf6-874a-d76aa4227cd2">SCARD_ATRMASK</a> structures specified by the <i>rgAtrMasks</i> parameter.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


### -param rgAtrMasks [in]

Array of 
<a href="https://msdn.microsoft.com/d7f1a747-a858-4bf6-874a-d76aa4227cd2">SCARD_ATRMASK</a> structures that contain the names of the cards for which to search.


### -param cAtrs [in]

Number of elements in the <i>rgAtrMasks</i> array.
					


### -param rgReaderStates [in, out]

Array of <a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a> structures that specify the readers to search, and receive the result.


### -param cReaders [in]

Number of elements in the <i>rgReaderStates</i> array.


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
Error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This service is especially useful when used in conjunction with 
<a href="https://msdn.microsoft.com/94776f3d-e8f0-4062-a766-2cf28cbfd050">SCardGetStatusChange</a>. If no matching cards are found by means of <a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a>, the calling application may use <b>SCardGetStatusChange</b> to wait for card availability changes.

The <b>SCardLocateCardsByATR</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> tracking function. For information about other tracking functions, see 
<a href="https://msdn.microsoft.com/b26b26bf-85ff-435f-a679-7529f19b1c1b">Smart Card Tracking Functions</a>.



