---
UID: NN:iads.IADsADSystemInfo
title: IADsADSystemInfo (iads.h)
description: The IADsADSystemInfo interface retrieves data about the local computer if it is running a Windows operating system in a Windows domain. For example, you can get the domain, site, and distinguished name of the local computer.
helpviewer_keywords: ["ADSystemInfo","IADsADSystemInfo","IADsADSystemInfo interface [ADSI]","IADsADSystemInfo interface [ADSI]","described","_ds_iadsadsysteminfo","adsi.iadsadsysteminfo","iads/IADsADSystemInfo"]
old-location: adsi\iadsadsysteminfo.htm
tech.root: adsi
ms.assetid: 5573d37b-10a8-4176-80c7-711552ff36cb
ms.date: 12/05/2018
ms.keywords: ADSystemInfo, IADsADSystemInfo, IADsADSystemInfo interface [ADSI], IADsADSystemInfo interface [ADSI],described, _ds_iadsadsysteminfo, adsi.iadsadsysteminfo, iads/IADsADSystemInfo
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
 - IADsADSystemInfo
 - iads/IADsADSystemInfo
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
 - IADsADSystemInfo
 - ADSystemInfo
---

# IADsADSystemInfo interface


## -description

The <b>IADsADSystemInfo</b> interface retrieves data about the local computer if it is running a Windows operating system in a Windows domain. For example, you can get the domain, site, and distinguished name of the local computer.

The <b>IADsADSystemInfo</b> interface is implemented on the <b>ADSystemInfo</b> object residing in adsldp.dll, which is included with the standard installation of ADSI on Windows 2000. You must explicitly create an instance of the <b>ADSystemInfo</b> object in order to call the methods on the <b>IADsADSystemInfo</b> interface. This requirement amounts to creating an <b>ADSystemInfo</b> instance with the  <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function in C/C++.

```cpp
IADsADSystemInfo *pADsys;
HRESULT hr = CoCreateInstance(CLSID_ADSystemInfo,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IADsADSystemInfo,
                              (void**)&pADsys);
```

You can also use the <b>New</b> operator in Visual Basic.

```vb
Dim adSys as New ADSystemInfo
```

Or you can call the <b>CreateObject</b> function in a scripting environment, supplying "ADSystemInfo" as the ProgID.

```vb
Dim adSys
Set adSys = CreateObject("ADSystemInfo")
```

## -inheritance

The <b>IADsADSystemInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsADSystemInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/ADSI/iadsadsysteminfo-property-methods">IADsADSystemInfo Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
