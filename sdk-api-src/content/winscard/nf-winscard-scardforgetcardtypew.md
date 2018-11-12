---
UID: NF:winscard.SCardForgetCardTypeW
title: SCardForgetCardTypeW function
author: windows-sdk-content
description: Removes an introduced smart card from the smart card subsystem.
old-location: security\scardforgetcardtype.htm
tech.root: secauthn
ms.assetid: 4f2d4791-d517-43e4-bff9-f88e12983dea
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SCardForgetCardType, SCardForgetCardType function [Security], SCardForgetCardTypeA, SCardForgetCardTypeW, _smart_scardforgetcardtype, security.scardforgetcardtype, winscard/SCardForgetCardType, winscard/SCardForgetCardTypeA, winscard/SCardForgetCardTypeW
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
req.unicode-ansi: SCardForgetCardTypeW (Unicode) and SCardForgetCardTypeA (ANSI)
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
 - SCardForgetCardType
 - SCardForgetCardTypeA
 - SCardForgetCardTypeW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardForgetCardTypeW function


## -description


The <b>SCardForgetCardType</b> function removes an introduced <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a>.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szCardName [in]

Display name of the card to be removed from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card database</a>.


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



This function is not redirected, but calling the function <b>SCardForgetCardType</b> when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardForgetCardType</b> function is a database management function. For more information about other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.


#### Examples

The following example removes the specified card type from the system. The example assumes that lReturn is a valid variable of type <b>LONG</b>,  that <i>hContext</i> is a valid handle received from a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function, and that "MyCardName" was  previously introduced by a call to the <a href="https://msdn.microsoft.com/1ac88466-1277-44d7-a471-b31d6bfce99e">SCardIntroduceCardType</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardForgetCardType(hContext, 
                              L"MyCardName");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetCardType\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/2022caff-ba01-4d0d-977c-3f51bde95659">SCardForgetReader</a>



<a href="https://msdn.microsoft.com/c6c98542-01b6-4b23-88cf-a619faee882e">SCardForgetReaderGroup</a>



<a href="https://msdn.microsoft.com/1ac88466-1277-44d7-a471-b31d6bfce99e">SCardIntroduceCardType</a>
 

 

