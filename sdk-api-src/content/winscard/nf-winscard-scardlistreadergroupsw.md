---
UID: NF:winscard.SCardListReaderGroupsW
title: SCardListReaderGroupsW function
author: windows-sdk-content
description: Provides the list of reader groups that have previously been introduced to the system.
old-location: security\scardlistreadergroups.htm
tech.root: secauthn
ms.assetid: df01fa4b-8053-4d3a-ae2e-66eeb6583225
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SCARD_ALL_READERS, SCARD_DEFAULT_READERS, SCARD_LOCAL_READERS, SCARD_SYSTEM_READERS, SCardListReaderGroups, SCardListReaderGroups function [Security], SCardListReaderGroupsA, SCardListReaderGroupsW, _smart_scardlistreadergroups, security.scardlistreadergroups, winscard/SCardListReaderGroups, winscard/SCardListReaderGroupsA, winscard/SCardListReaderGroupsW
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
req.unicode-ansi: SCardListReaderGroupsW (Unicode) and SCardListReaderGroupsA (ANSI)
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
 - SCardListReaderGroups
 - SCardListReaderGroupsA
 - SCardListReaderGroupsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SCardListReaderGroupsW
: 
---

# SCardListReaderGroupsW function


## -description


The <b>SCardListReaderGroups</b> function provides the list of <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader groups</a> that have previously been introduced to the system.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. 

If this parameter is set to <b>NULL</b>, the search for reader groups is not limited to any context.


### -param mszGroups [out]

Multi-string that lists the reader groups defined to the system and available to the current user on the current <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">terminal</a>. If this value is <b>NULL</b>, <b>SCardListReaderGroups</b> ignores the buffer length supplied in <i>pcchGroups</i>, writes the length of the buffer that would have been returned if this parameter had not been <b>NULL</b> to <i>pcchGroups</i>, and returns a success code.

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
 


### -param pcchGroups [in, out]

Length of the <i>mszGroups</i> buffer in characters, and receives the actual length of the multi-string structure, including all trailing <b>null</b> characters. If the buffer length is specified as SCARD_AUTOALLOCATE, then <i>mszGroups</i> is converted to a pointer to a byte pointer, and receives the address of a block of memory containing the multi-string structure. This block of memory must be deallocated with 
<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>.


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
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



A group is returned only if it contains at least one <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>. This includes the group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">SCard$DefaultReaders</a>. The group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">SCard$AllReaders</a> cannot be returned, since it only exists implicitly.

The <b>SCardListReaderGroups</b> function is a database query function. For more information on other database query functions, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a>.


#### Examples

The following example  shows listing the reader groups.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LPTSTR          pmszReaderGroups = NULL;
LPTSTR          pReaderGroup;
LONG            lReturn;
DWORD           cch = SCARD_AUTOALLOCATE;
    
// Retrieve the list the reader groups.
// hSC was set by a previous call to SCardEstablishContext.
lReturn = SCardListReaderGroups(hSC,
                                (LPTSTR)&amp;pmszReaderGroups,
                                &amp;cch );
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardListReaderGroups\n");
else
{
    // Do something with the multi string of reader groups.
    // Output the values.
    // A double-null terminates the list of values.
    pReaderGroup = pmszReaderGroups;
    while ( '\0' != *pReaderGroup )
    {
        // Display the value.
        printf("%S\n", pReaderGroup );
        // Advance to the next value.
        pReaderGroup = pReaderGroup + wcslen((wchar_t *) pReaderGroup) + 1;
    }

    // Remember to free pmszReaderGroups by a call to SCardFreeMemory.
    // ...
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>



<a href="https://msdn.microsoft.com/6e0f42af-9ac1-469b-b241-939d64676d99">SCardGetProviderId</a>



<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>



<a href="https://msdn.microsoft.com/2460c133-3ad4-4f73-9f55-56fc3bab9cdb">SCardListInterfaces</a>



<a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a>
 

 

