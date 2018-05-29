---
UID: NF:winscard.SCardForgetReaderA
title: SCardForgetReaderA function
author: windows-sdk-content
description: Removes a previously introduced reader from control by the smart card subsystem. It is removed from the smart card database, including from any reader group that it may have been added to.
old-location: security\scardforgetreader.htm
old-project: SecAuthN
ms.assetid: 2022caff-ba01-4d0d-977c-3f51bde95659
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SCardForgetReader, SCardForgetReader function [Security], SCardForgetReaderA, SCardForgetReaderW, _smart_scardforgetreader, security.scardforgetreader, winscard/SCardForgetReader, winscard/SCardForgetReaderA, winscard/SCardForgetReaderW
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
req.unicode-ansi: SCardForgetReaderW (Unicode) and SCardForgetReaderA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WINSAT_BITMAP_SIZE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Winscard.dll
api_name:
-	SCardForgetReader
-	SCardForgetReaderA
-	SCardForgetReaderW
product: Windows
targetos: Windows
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# SCardForgetReaderA function


## -description


The <b>SCardForgetReader</b> function removes a previously introduced <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> from control by the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card subsystem</a>. It is removed from the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card database</a>, including from any <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader group</a> that it may have been added to.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szReaderName [in]

Display name of the reader to be removed from the smart card database.


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



If the specified reader is the last member of a reader group, the reader group is automatically removed as well.

The <b>SCardForgetReader</b> function is a database management function. For more information on other database management functions, see 
<a href="https://msdn.microsoft.com/a2f457e1-c042-42e7-9071-cf0edd68e27a">Smart Card Database Management Functions</a>.


#### Examples

The following example removes the display name of the specified card reader from the system. The example assumes that lReturn is a valid variable of type <b>LONG</b> and that hContext is a valid handle received from a previous call to the <a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a> function.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
lReturn = SCardForgetReader(hContext, 
                            TEXT("MyReader"));
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetReader\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf9b005-b76c-4fc9-b4bd-a1ad8552535f">SCardEstablishContext</a>



<a href="https://msdn.microsoft.com/4f2d4791-d517-43e4-bff9-f88e12983dea">SCardForgetCardType</a>



<a href="https://msdn.microsoft.com/c6c98542-01b6-4b23-88cf-a619faee882e">SCardForgetReaderGroup</a>



<a href="https://msdn.microsoft.com/1f8b9d75-5bba-40c3-99a0-6910855fcd4d">SCardIntroduceReader</a>
 

 

