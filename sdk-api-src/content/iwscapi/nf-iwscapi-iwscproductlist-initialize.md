---
UID: NF:iwscapi.IWSCProductList.Initialize
title: IWSCProductList::Initialize
author: windows-sdk-content
description: Gathers information on all of the providers of the specified type on the computer.
old-location: winprog\iwscproductlist_initialize.htm
old-project: devnotes
ms.assetid: 0D003510-BCFE-45E9-A34E-58036C382157
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWSCProductList interface [Windows API],Initialize method, IWSCProductList.Initialize, IWSCProductList::Initialize, Initialize, Initialize method [Windows API], Initialize method [Windows API],IWSCProductList interface, WSC_SECURITY_PROVIDER_ANTISPYWARE, WSC_SECURITY_PROVIDER_ANTIVIRUS, WSC_SECURITY_PROVIDER_FIREWALL, iwscapi/IWSCProductList::Initialize, winprog.iwscproductlist_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: WSC_SECURITY_SIGNATURE_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wscapi.dll
api_name:
 - IWSCProductList.Initialize
product: Windows
targetos: Windows
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IWSCProductList::Initialize


## -description


Gathers information on all of the providers of the specified type on the computer.


## -parameters




### -param provider [in]

A value from the  <a href="https://msdn.microsoft.com/b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187">WSC_SECURITY_PROVIDER</a> enumeration with the name of the provider as one of the following values. Note that the possible values can't be combined in a logical OR as they can when used with the <a href="https://msdn.microsoft.com/1193eba3-a01b-4ee3-a83d-25dcdbc15de0">WscGetSecurityProviderHealth</a> function.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WSC_SECURITY_PROVIDER_ANTIVIRUS"></a><a id="wsc_security_provider_antivirus"></a><dl>
<dt><b>WSC_SECURITY_PROVIDER_ANTIVIRUS</b></dt>
</dl>
</td>
<td width="60%">
Antivirus products.

</td>
</tr>
<tr>
<td width="40%"><a id="WSC_SECURITY_PROVIDER_ANTISPYWARE"></a><a id="wsc_security_provider_antispyware"></a><dl>
<dt><b>WSC_SECURITY_PROVIDER_ANTISPYWARE</b></dt>
</dl>
</td>
<td width="60%">
Anti-spyware products. 

</td>
</tr>
<tr>
<td width="40%"><a id="WSC_SECURITY_PROVIDER_FIREWALL"></a><a id="wsc_security_provider_firewall"></a><dl>
<dt><b>WSC_SECURITY_PROVIDER_FIREWALL</b></dt>
</dl>
</td>
<td width="60%">
Firewall products. 

</td>
</tr>
</table>
 


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -remarks



Once the client gets an <a href="https://msdn.microsoft.com/81BC78F1-6F95-49D3-8EDD-EB7E13119A86">IWSCProductList</a> pointer, they must call <b>Initialize</b> with a provider type, which gathers information on all the providers of that type installed on the system. Only one type of provider can be specified when calling <b>Initialize</b>, and the <b>Initialize</b> method may only be called once for each instance of an <b>IWSCProductList</b> pointer.  After the list has been initialized, the user is free to call <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> to obtain the number of providers in the list and <a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a> to retrieve an individual provider.




## -see-also




<a href="https://msdn.microsoft.com/81BC78F1-6F95-49D3-8EDD-EB7E13119A86">IWSCProductList</a>
 

 

