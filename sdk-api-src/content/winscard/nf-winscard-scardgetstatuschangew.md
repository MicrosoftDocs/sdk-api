---
UID: NF:winscard.SCardGetStatusChangeW
title: SCardGetStatusChangeW function
author: windows-sdk-content
description: Blocks execution until the current availability of the cards in a specific set of readers changes.
old-location: security\scardgetstatuschange.htm
old-project: SecAuthN
ms.assetid: 94776f3d-e8f0-4062-a766-2cf28cbfd050
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: SCardGetStatusChange, SCardGetStatusChange function [Security], SCardGetStatusChangeA, SCardGetStatusChangeW, _smart_scardgetstatuschange, security.scardgetstatuschange, winscard/SCardGetStatusChange, winscard/SCardGetStatusChangeA, winscard/SCardGetStatusChangeW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SCardGetStatusChangeW (Unicode) and SCardGetStatusChangeA (ANSI)
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
 - Ext-MS-Win-wlan-scard-l1-1-0.dll
 - Ext-MS-Win-Security-WinSCard-L1-1-0.dll
api_name:
 - SCardGetStatusChange
 - SCardGetStatusChangeA
 - SCardGetStatusChangeW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardGetStatusChangeW function


## -description


The <b>SCardGetStatusChange</b> function blocks execution until the current availability of the cards in a specific set of readers changes.

The caller supplies a list of <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">readers</a> to be monitored by an SCARD_READERSTATE array and the maximum amount of time (in milliseconds) that it is willing to wait for an action to occur on one of the listed readers. Note that <b>SCardGetStatusChange</b> uses the user-supplied value in the <b>dwCurrentState</b> members of the <i>rgReaderStates</i>
<a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a> array as the definition of the current <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the readers. The function returns when there is a change in availability, having filled in the <b>dwEventState</b> members of <i>rgReaderStates</i> appropriately.


## -parameters




### -param hContext [in]

A handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function.


### -param dwTimeout [in]

The maximum amount of time, in milliseconds, to wait for an action. A value of zero causes the function to return immediately. A value of INFINITE causes this function never to time out.


### -param rgReaderStates [in, out]

An array of 
<a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a> structures that specify the readers to watch, and that receives the result.

To be notified of the arrival of a new smart card reader, set the <b>szReader</b> member of a <a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a> structure to "\\\\?PnP?\\Notification", and set all of the other members of that structure to zero.

<div class="alert"><b>Important</b>  Each member of each structure in this array must be initialized to zero and then set to specific values as necessary. If this is not done, the function will fail in situations that involve remote card readers.</div>
<div> </div>

### -param cReaders [in]

The number of elements in the <i>rgReaderStates</i> array.


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



The <b>SCardGetStatusChange</b> function is a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> tracking function. For more information about other tracking functions, see 
<a href="https://msdn.microsoft.com/b26b26bf-85ff-435f-a679-7529f19b1c1b">Smart Card Tracking Functions</a>.


#### Examples

For information about how to call this function, see the  example in 
<a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/4e9bbed7-f899-4361-a526-029a710d5147">SCARD_READERSTATE</a>



<a href="https://msdn.microsoft.com/abf3b4ff-4775-40e9-b68d-97dcf6a892ba">SCardCancel</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/7ee90188-6fe5-417b-a7c7-9c29d9cdd4d0">SCardLocateCards</a>
 

 

