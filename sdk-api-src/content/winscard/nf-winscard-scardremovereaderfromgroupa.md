---
UID: NF:winscard.SCardRemoveReaderFromGroupA
title: SCardRemoveReaderFromGroupA function
author: windows-sdk-content
description: Removes a reader from an existing reader group. This function has no effect on the reader.
old-location: security\scardremovereaderfromgroup.htm
old-project: secauthn
ms.assetid: a9bdaf16-1a6f-4a84-ab29-3d6df9003ff9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardRemoveReaderFromGroup, SCardRemoveReaderFromGroup function [Security], SCardRemoveReaderFromGroupA, SCardRemoveReaderFromGroupW, _smart_scardremovereaderfromgroup, security.scardremovereaderfromgroup, winscard/SCardRemoveReaderFromGroup, winscard/SCardRemoveReaderFromGroupA, winscard/SCardRemoveReaderFromGroupW
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
req.unicode-ansi: SCardRemoveReaderFromGroupW (Unicode) and SCardRemoveReaderFromGroupA (ANSI)
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
 - SCardRemoveReaderFromGroup
 - SCardRemoveReaderFromGroupA
 - SCardRemoveReaderFromGroupW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardRemoveReaderFromGroupA function


## -description


The <b>SCardRemoveReaderFromGroup</b> function removes a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> from an existing <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader group</a>. This function has no effect on the reader.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szReaderName [in]

Display name of the reader to be removed.


### -param szGroupName [in]

Display name of the group from which the reader should be removed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ALL_READERS"></a><a id="scard_all_readers"></a><dl>
<dt><b>SCARD_ALL_READERS</b></dt>
<dt>TEXT("SCard$AllReaders\000")</dt>
</dl>
</td>
<td width="60%">
Group used when no group name is provided when listing readers. Returns a list of all readers, regardless of what group or groups the readers are in.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_DEFAULT_READERS"></a><a id="scard_default_readers"></a><dl>
<dt><b>SCARD_DEFAULT_READERS</b></dt>
<dt>TEXT("SCard$DefaultReaders\000")</dt>
</dl>
</td>
<td width="60%">
Default group to which all readers are added when introduced into the system.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_LOCAL_READERS"></a><a id="scard_local_readers"></a><dl>
<dt><b>SCARD_LOCAL_READERS</b></dt>
<dt>TEXT("SCard$LocalReaders\000")</dt>
</dl>
</td>
<td width="60%">
Unused legacy value. This is an internally managed group that cannot be modified by using any reader group APIs. It is intended to be used for enumeration only.

</td>
</tr>
<tr>
<td width="40%"><a id="SCARD_SYSTEM_READERS"></a><a id="scard_system_readers"></a><dl>
<dt><b>SCARD_SYSTEM_READERS</b></dt>
<dt>TEXT("SCard$SystemReaders\000")</dt>
</dl>
</td>
<td width="60%">
Unused legacy value. This is an internally managed group that cannot be modified by using any reader group APIs. It is intended to be used for enumeration only.

</td>
</tr>
</table>
 


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



When the last reader is removed from a group, the group is automatically forgotten.

The <b>SCardRemoveReaderFromGroup</b> function is a database management function. For information about other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.

To add a reader to a reader group, use 
<a href="https://msdn.microsoft.com/f2f5fcd8-3b60-4c8a-b92c-c63be970cc35">SCardAddReaderToGroup</a>.


#### Examples

The following example  shows how to remove a reader from the group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Remove a reader from the group.
// lReturn is of type LONG.
// hContext was set by a previous call to SCardEstablishContext.
// The group is automatically forgotten if no readers remain in it.
lReturn = SCardRemoveReaderFromGroup(hContext, 
                                     L"MyReader",
                                     L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardRemoveReaderFromGroup\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f2f5fcd8-3b60-4c8a-b92c-c63be970cc35">SCardAddReaderToGroup</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/4f2d4791-d517-43e4-bff9-f88e12983dea">SCardForgetCardType</a>



<a href="https://msdn.microsoft.com/2022caff-ba01-4d0d-977c-3f51bde95659">SCardForgetReader</a>



<a href="https://msdn.microsoft.com/c6c98542-01b6-4b23-88cf-a619faee882e">SCardForgetReaderGroup</a>
 

 

