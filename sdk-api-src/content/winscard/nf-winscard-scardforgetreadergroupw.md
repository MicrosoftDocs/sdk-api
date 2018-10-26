---
UID: NF:winscard.SCardForgetReaderGroupW
title: SCardForgetReaderGroupW function
author: windows-sdk-content
description: Removes a previously introduced smart card reader group from the smart card subsystem. Although this function automatically clears all readers from the group, it does not affect the existence of the individual readers in the database.
old-location: security\scardforgetreadergroup.htm
tech.root: secauthn
ms.assetid: c6c98542-01b6-4b23-88cf-a619faee882e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardForgetReaderGroup, SCardForgetReaderGroup function [Security], SCardForgetReaderGroupA, SCardForgetReaderGroupW, _smart_scardforgetreadergroup, security.scardforgetreadergroup, winscard/SCardForgetReaderGroup, winscard/SCardForgetReaderGroupA, winscard/SCardForgetReaderGroupW
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
req.unicode-ansi: SCardForgetReaderGroupW (Unicode) and SCardForgetReaderGroupA (ANSI)
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
 - SCardForgetReaderGroup
 - SCardForgetReaderGroupA
 - SCardForgetReaderGroupW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardForgetReaderGroupW function


## -description


The <b>SCardForgetReaderGroup</b> function removes a previously introduced <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader group</a> from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a>. Although this function automatically clears all readers from the group, it does not affect the existence of the individual <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">readers</a> in the database.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szGroupName [in]

Display name of the reader group to be removed. System-defined reader groups cannot be removed from the database.

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



The <b>SCardForgetReaderGroup</b> function is a database management function. For more information on other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.


#### Examples

The following example shows how to remove a reader group from the system. The example assumes that lReturn is an existing variable of type <b>LONG</b>, and that hContext is a valid handle to a resource manager context previously obtained from a call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardForgetReaderGroup(hContext, 
                                 L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetReaderGroup\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/4f2d4791-d517-43e4-bff9-f88e12983dea">SCardForgetCardType</a>



<a href="https://msdn.microsoft.com/2022caff-ba01-4d0d-977c-3f51bde95659">SCardForgetReader</a>



<a href="https://msdn.microsoft.com/aaf7d2f9-71d5-42bb-a96f-71124be40aa3">SCardIntroduceReaderGroup</a>
 

 

