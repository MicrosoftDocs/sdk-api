---
UID: NF:winscard.SCardForgetCardTypeW
title: SCardForgetCardTypeW function (winscard.h)
description: Removes an introduced smart card from the smart card subsystem.helpviewer_keywords: ["SCardForgetCardType","SCardForgetCardType function [Security]","SCardForgetCardTypeA","SCardForgetCardTypeW","_smart_scardforgetcardtype","security.scardforgetcardtype","winscard/SCardForgetCardType","winscard/SCardForgetCardTypeA","winscard/SCardForgetCardTypeW"]
old-location: security\scardforgetcardtype.htm
tech.root: SecAuthN
ms.assetid: 4f2d4791-d517-43e4-bff9-f88e12983dea
ms.date: 12/05/2018
ms.keywords: SCardForgetCardType, SCardForgetCardType function [Security], SCardForgetCardTypeA, SCardForgetCardTypeW, _smart_scardforgetcardtype, security.scardforgetcardtype, winscard/SCardForgetCardType, winscard/SCardForgetCardTypeA, winscard/SCardForgetCardTypeW
f1_keywords:
- winscard/SCardForgetCardType
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SCardForgetCardTypeW function


## -description


The <b>SCardForgetCardType</b> function removes an introduced <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">smart card</a> from the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">smart card subsystem</a>.


## -parameters




### -param hContext [in]

Handle that identifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">resource manager context</a>. The resource manager context is set by a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>. This parameter cannot be <b>NULL</b>.


### -param szCardName [in]

Display name of the card to be removed from the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">smart card database</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



This function is not redirected, but calling the function <b>SCardForgetCardType</b> when inside a Remote Desktop session  will not result in an error. It only means that the result will be from the remote computer instead of the local computer. 

The <b>SCardForgetCardType</b> function is a database management function. For more information about other database management functions, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/smart-card-database-management-functions">Smart Card Database Management Functions</a>.


#### Examples

The following example removes the specified card type from the system. The example assumes that lReturn is a valid variable of type <b>LONG</b>,  that <i>hContext</i> is a valid handle received from a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a> function, and that "MyCardName" was  previously introduced by a call to the <a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardintroducecardtypea">SCardIntroduceCardType</a> function.


```cpp

lReturn = SCardForgetCardType(hContext, 
                              L"MyCardName");
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardForgetCardType\n");

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardestablishcontext">SCardEstablishContext</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardforgetreadera">SCardForgetReader</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardforgetreadergroupa">SCardForgetReaderGroup</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winscard/nf-winscard-scardintroducecardtypea">SCardIntroduceCardType</a>
 

 

