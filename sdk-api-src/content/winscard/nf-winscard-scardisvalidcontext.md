---
UID: NF:winscard.SCardIsValidContext
title: SCardIsValidContext function
author: windows-sdk-content
description: Determines whether a smart card context handle is valid.
old-location: security\scardisvalidcontext.htm
tech.root: secauthn
ms.assetid: 50bcb6aa-6265-4035-8265-45990f791ce3
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: SCardIsValidContext, SCardIsValidContext function [Security], _smart_scardisvalidcontext, security.scardisvalidcontext, winscard/SCardIsValidContext
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
req.unicode-ansi: 
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
 - SCardIsValidContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardIsValidContext function


## -description


The <b>SCardIsValidContext</b> function determines whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> context handle is valid.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context can be set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCARD_S_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The <i>hContext</i> parameter is valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hContext</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other values</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



Call this function to determine whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> context handle is still valid. After a smart card context handle has been set by 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>, it may become not valid if the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager</a> service has been shut down.


#### Examples

The following example  shows determining whether a smart card context handle is valid.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Check the smart card context handle.
// hContext was set previously by SCardEstablishContext.

LONG    lReturn;
lReturn = SCardIsValidContext(hContext);
if ( SCARD_S_SUCCESS != lReturn )
{
    // Function failed; check return value.
    if ( ERROR_INVALID_HANDLE == lReturn )
        printf("Handle is invalid\n");
    else
    {
        // Some unexpected error occurred; report and bail out.
        printf("Failed SCardIsValidContext - %x\n", lReturn);
        exit(1);  // Or other appropriate error action.
    }
}
else
{
    // Handle is valid; proceed as needed.
    // ...
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>
 

 

