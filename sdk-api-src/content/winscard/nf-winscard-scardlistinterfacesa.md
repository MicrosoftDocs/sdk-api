---
UID: NF:winscard.SCardListInterfacesA
title: SCardListInterfacesA function
author: windows-sdk-content
description: Provides a list of interfaces supplied by a given card.
old-location: security\scardlistinterfaces.htm
tech.root: secauthn
ms.assetid: 2460c133-3ad4-4f73-9f55-56fc3bab9cdb
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: SCardListInterfaces, SCardListInterfaces function [Security], SCardListInterfacesA, SCardListInterfacesW, _smart_scardlistinterfaces, security.scardlistinterfaces, winscard/SCardListInterfaces, winscard/SCardListInterfacesA, winscard/SCardListInterfacesW
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
req.unicode-ansi: SCardListInterfacesW (Unicode) and SCardListInterfacesA (ANSI)
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
 - SCardListInterfaces
 - SCardListInterfacesA
 - SCardListInterfacesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardListInterfacesA function


## -description


The <b>SCardListInterfaces</b> function provides a list of interfaces supplied by a given card.

The caller supplies the name of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> previously introduced to the subsystem, and receives the list of interfaces supported by the card.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> for the query. The resource manager context can be set by a previous call to <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szCard [in]

Name of the smart card already introduced to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a>.


### -param pguidInterfaces [out]

Array of interface identifiers (GUIDs) that indicate the interfaces supported by the smart card. If this value is <b>NULL</b>, <b>SCardListInterfaces</b> ignores the array length supplied in <i>pcguidInterfaces</i>, returning the size of the array that would have been returned if this parameter had not been <b>NULL</b> to <i>pcguidInterfaces</i> and a success code.


### -param pcguidInterfaces [in, out]

Size of the <i>pcguidInterfaces</i> array, and receives the actual size of the returned array. If the array size is specified as SCARD_AUTOALLOCATE, then <i>pcguidInterfaces</i> is converted to a pointer to a GUID pointer, and receives the address of a block of memory containing the array. This block of memory must be deallocated with 
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
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected, but calling the function when attempting a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardListInterfaces</b> function is a database query function. For more information on other database query functions, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a>.


#### Examples

The following example  shows listing the interfaces for a smart card.


```cpp
LPGUID          pGuids = NULL;
LONG            lReturn;
DWORD           cGuid = SCARD_AUTOALLOCATE;

// Retrieve the list of interfaces.
lReturn = SCardListInterfaces(NULL,
                              (LPCSTR) "MyCard",
                              (LPGUID)&pGuids,
                              &cGuid );
if ( SCARD_S_SUCCESS != lReturn )
{
    printf("Failed SCardListInterfaces\n");
    exit(1);   // Or other appropriate action
}

if ( 0 != cGuid )
{
    // Do something with the array of Guids.
    // Remember to free pGuids when done (by SCardFreeMemory).
    // ...
}

```





## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/d41d3891-671b-4129-8034-b251af983830">SCardFreeMemory</a>



<a href="https://msdn.microsoft.com/6e0f42af-9ac1-469b-b241-939d64676d99">SCardGetProviderId</a>



<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>



<a href="https://msdn.microsoft.com/df01fa4b-8053-4d3a-ae2e-66eeb6583225">SCardListReaderGroups</a>



<a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a>
 

 

