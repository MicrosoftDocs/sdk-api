---
UID: NF:winscard.SCardGetProviderIdW
title: SCardGetProviderIdW function
author: windows-sdk-content
description: Returns the identifier (GUID) of the primary service provider for a given card.
old-location: security\scardgetproviderid.htm
old-project: secauthn
ms.assetid: 6e0f42af-9ac1-469b-b241-939d64676d99
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: SCardGetProviderId, SCardGetProviderId function [Security], SCardGetProviderIdA, SCardGetProviderIdW, _smart_scardgetproviderid, security.scardgetproviderid, winscard/SCardGetProviderId, winscard/SCardGetProviderIdA, winscard/SCardGetProviderIdW
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
req.unicode-ansi: SCardGetProviderIdW (Unicode) and SCardGetProviderIdA (ANSI)
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
 - SCardGetProviderId
 - SCardGetProviderIdA
 - SCardGetProviderIdW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardGetProviderIdW function


## -description


The <b>SCardGetProviderId</b> function returns the identifier (GUID) of the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary service provider</a> for a given card.

The caller supplies the name of a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> (previously introduced to the system) and receives the registered identifier of the primary service provider GUID, if one exists.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a> for the query. The resource manager context can be set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szCard [in]

Name of the card defined to the system.


### -param pguidProviderId [out]

Identifier (GUID) of the primary service provider. This provider may be activated using COM, and will supply access to other services in the card.


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



This function is not redirected, but calling the function when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardGetProviderId</b> function is a database query function. For more information on other database query functions, see 
<a href="https://msdn.microsoft.com/a30cbb99-522c-4752-bfcd-75be608785f1">Smart Card Database Query Functions</a>.


#### Examples

The following example shows how to get the provider ID for the specified card. The example assumes that hContext is a valid handle obtained from a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function and that "MyCardName" was introduced by a previous call to the <a href="https://msdn.microsoft.com/1ac88466-1277-44d7-a471-b31d6bfce99e">SCardIntroduceCardType</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>GUID    guidProv;
LONG    lReturn;

lReturn = SCardGetProviderId(hContext, 
                             L"MyCardName",
                             &amp;guidProv);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardGetProviderId - %x\n", lReturn);
else
{
    // Use the provider GUID as needed.
    // ...
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/b8ecbb8c-e1fb-485b-9a2c-20e6edf25cf1">SCardListCards</a>



<a href="https://msdn.microsoft.com/2460c133-3ad4-4f73-9f55-56fc3bab9cdb">SCardListInterfaces</a>



<a href="https://msdn.microsoft.com/df01fa4b-8053-4d3a-ae2e-66eeb6583225">SCardListReaderGroups</a>



<a href="https://msdn.microsoft.com/b50218f1-e960-4838-b44b-6c71fa94a0ad">SCardListReaders</a>
 

 

