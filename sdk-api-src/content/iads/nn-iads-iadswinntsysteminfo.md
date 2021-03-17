---
UID: NN:iads.IADsWinNTSystemInfo
title: IADsWinNTSystemInfo (iads.h)
description: The IADsWinNTSystemInfo interface retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.
helpviewer_keywords: ["IADsWinNTSystemInfo","IADsWinNTSystemInfo interface [ADSI]","IADsWinNTSystemInfo interface [ADSI]","described","_ds_iadswinntsysteminfo","adsi.iadswinntsysteminfo","iads/IADsWinNTSystemInfo"]
old-location: adsi\iadswinntsysteminfo.htm
tech.root: adsi
ms.assetid: 63a20250-1b93-49df-b7f8-7169db8efde0
ms.date: 12/05/2018
ms.keywords: IADsWinNTSystemInfo, IADsWinNTSystemInfo interface [ADSI], IADsWinNTSystemInfo interface [ADSI],described, _ds_iadswinntsysteminfo, adsi.iadswinntsysteminfo, iads/IADsWinNTSystemInfo
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsWinNTSystemInfo
 - iads/IADsWinNTSystemInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsWinNTSystemInfo
---

# IADsWinNTSystemInfo interface


## -description

The <b>IADsWinNTSystemInfo</b> interface  retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.

The <b>IADsWinNTSystemInfo</b> interface is implemented on the <b>WinNTSystemInfo</b> object residing in Activeds.dll, which is included in the standard installation of ADSI for domain-capable editions of Windows. You must explicitly create an instance of the <b>WinNTSystemInfo</b> object to call the methods on the <b>IADsWinNTSystemInfo</b> interface. This requirement means creating an <b>WinNTSystemInfo</b> instance with the  <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function in C/C++.

```cpp
IADsWinNTSystemInfo *pNTsys;
HRESULT hr = CoCreateInstance(CLSID_WinNTSystemInfo,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IADsWinNTSystemInfo,
                              (void**)&pNTsys);
```

You can also use the <b>New</b> operator in Visual Basic.

```vb
Dim ntSys As New WinNTSystemInfo
```

You can also call the <b>CreateObject</b> function in a scripting environment, supplying "WinNTSystemInfo" as the ProgID.

```vb
Dim ntSys
Set ntSys = CreateObject("WinNTSystemInfo")
```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/ADSI/iadswinntsysteminfo-property-methods">IADsWinNTSystemInfo Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>