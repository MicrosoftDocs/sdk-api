---
UID: NF:winscard.SCardIntroduceReaderGroupW
title: SCardIntroduceReaderGroupW function
author: windows-sdk-content
description: Introduces a reader group to the smart card subsystem. However, the reader group is not created until the group is specified when adding a reader to the smart card database.
old-location: security\scardintroducereadergroup.htm
old-project: SecAuthN
ms.assetid: aaf7d2f9-71d5-42bb-a96f-71124be40aa3
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardIntroduceReaderGroup, SCardIntroduceReaderGroup function [Security], SCardIntroduceReaderGroupA, SCardIntroduceReaderGroupW, _smart_scardintroducereadergroup, security.scardintroducereadergroup, winscard/SCardIntroduceReaderGroup, winscard/SCardIntroduceReaderGroupA, winscard/SCardIntroduceReaderGroupW
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
req.unicode-ansi: SCardIntroduceReaderGroupW (Unicode) and SCardIntroduceReaderGroupA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winscard.dll
api_name:
-	SCardIntroduceReaderGroup
-	SCardIntroduceReaderGroupA
-	SCardIntroduceReaderGroupW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardIntroduceReaderGroupW function


## -description


The <b>SCardIntroduceReaderGroup</b> function introduces a <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader group</a> to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> subsystem. However, the reader group is not created until the group is specified when adding a reader to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card database</a>.


## -parameters




### -param hContext [in]

Supplies the handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function. If this parameter is <b>NULL</b>, the scope of the resource manager is SCARD_SCOPE_SYSTEM.


### -param szGroupName [in]

Supplies the display name to be assigned to the new reader group.

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



The <b>SCardIntroduceReaderGroup</b> function is provided for PC/SC specification compatibility. Reader groups are not stored until a reader is added to the group.

The <b>SCardIntroduceReaderGroup</b> function is a database management function. For a description of other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.

To remove a reader group, use 
<a href="https://msdn.microsoft.com/c6c98542-01b6-4b23-88cf-a619faee882e">SCardForgetReaderGroup</a>.


#### Examples

The following example  shows introducing a smart card reader group.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Introduce the reader group.
// lReturn is of type LONG.
// hContext was set by a previous call to SCardEstablishContext.
lReturn = SCardIntroduceReaderGroup(hContext, 
                                    L"MyReaderGroup");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardIntroduceReaderGroup\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f2f5fcd8-3b60-4c8a-b92c-c63be970cc35">SCardAddReaderToGroup</a>



<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/c6c98542-01b6-4b23-88cf-a619faee882e">SCardForgetReaderGroup</a>



<a href="https://msdn.microsoft.com/1ac88466-1277-44d7-a471-b31d6bfce99e">SCardIntroduceCardType</a>



<a href="https://msdn.microsoft.com/1f8b9d75-5bba-40c3-99a0-6910855fcd4d">SCardIntroduceReader</a>
 

 

