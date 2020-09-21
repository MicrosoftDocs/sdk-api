---
UID: NF:iwscapi.IWSCProductList.Initialize
title: IWSCProductList::Initialize (iwscapi.h)
description: Gathers information on all of the providers of the specified type on the computer.
helpviewer_keywords: ["IWSCProductList interface [Windows API]","Initialize method","IWSCProductList.Initialize","IWSCProductList::Initialize","Initialize","Initialize method [Windows API]","Initialize method [Windows API]","IWSCProductList interface","WSC_SECURITY_PROVIDER_ANTISPYWARE","WSC_SECURITY_PROVIDER_ANTIVIRUS","WSC_SECURITY_PROVIDER_FIREWALL","iwscapi/IWSCProductList::Initialize","winprog.iwscproductlist_initialize"]
old-location: winprog\iwscproductlist_initialize.htm
tech.root: winprog
ms.assetid: 0D003510-BCFE-45E9-A34E-58036C382157
ms.date: 12/05/2018
ms.keywords: IWSCProductList interface [Windows API],Initialize method, IWSCProductList.Initialize, IWSCProductList::Initialize, Initialize, Initialize method [Windows API], Initialize method [Windows API],IWSCProductList interface, WSC_SECURITY_PROVIDER_ANTISPYWARE, WSC_SECURITY_PROVIDER_ANTIVIRUS, WSC_SECURITY_PROVIDER_FIREWALL, iwscapi/IWSCProductList::Initialize, winprog.iwscproductlist_initialize
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
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSCProductList::Initialize
 - iwscapi/IWSCProductList::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wscapi.dll
api_name:
 - IWSCProductList.Initialize
---

# IWSCProductList::Initialize


## -description

Gathers information on all of the providers of the specified type on the computer.

## -parameters

### -param provider [in]

A value from the  <a href="/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider">WSC_SECURITY_PROVIDER</a> enumeration with the name of the provider as one of the following values. Note that the possible values can't be combined in a logical OR as they can when used with the <a href="/windows/desktop/api/wscapi/nf-wscapi-wscgetsecurityproviderhealth">WscGetSecurityProviderHealth</a> function.

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

Once the client gets an <a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproductlist">IWSCProductList</a> pointer, they must call <b>Initialize</b> with a provider type, which gathers information on all the providers of that type installed on the system. Only one type of provider can be specified when calling <b>Initialize</b>, and the <b>Initialize</b> method may only be called once for each instance of an <b>IWSCProductList</b> pointer.  After the list has been initialized, the user is free to call <a href="/windows/desktop/api/iwscapi/nf-iwscapi-iwscproductlist-get_count">Count</a> to obtain the number of providers in the list and <a href="/windows/desktop/api/iwscapi/nf-iwscapi-iwscproductlist-get_item">Item</a> to retrieve an individual provider.

## -see-also

<a href="/windows/desktop/api/iwscapi/nn-iwscapi-iwscproductlist">IWSCProductList</a>