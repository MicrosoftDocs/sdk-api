---
UID: NF:winscard.SCardFreeMemory
title: SCardFreeMemory function
author: windows-sdk-content
description: Releases memory that has been returned from the resource manager using the SCARD_AUTOALLOCATE length designator.
old-location: security\scardfreememory.htm
old-project: SecAuthN
ms.assetid: d41d3891-671b-4129-8034-b251af983830
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SCardFreeMemory, SCardFreeMemory function [Security], _smart_scardfreememory, security.scardfreememory, winscard/SCardFreeMemory
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
req.unicode-ansi: 
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
 - SCardFreeMemory
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardFreeMemory function


## -description


The <b>SCardFreeMemory</b> function releases memory that has been returned from the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a> using the SCARD_AUTOALLOCATE length designator.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> returned from <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>, or <b>NULL</b> if the creating function also specified <b>NULL</b> for its <i>hContext</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a>.
					


### -param pvMem [in]

Memory block to be released.


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
<a href="https://docs.microsoft.com/windows/desktop//SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/6e0f42af-9ac1-469b-b241-939d64676d99">SCardGetProviderId</a>



<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>



<a href="https://msdn.microsoft.com/2460c133-3ad4-4f73-9f55-56fc3bab9cdb">SCardListInterfaces</a>



<a href="https://msdn.microsoft.com/df01fa4b-8053-4d3a-ae2e-66eeb6583225">SCardListReaderGroups</a>



<a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a>
 

 

