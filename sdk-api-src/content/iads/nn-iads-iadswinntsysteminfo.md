---
UID: NN:iads.IADsWinNTSystemInfo
title: IADsWinNTSystemInfo
author: windows-sdk-content
description: The IADsWinNTSystemInfo interface retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.
old-location: adsi\iadswinntsysteminfo.htm
tech.root: ADSI
ms.assetid: 63a20250-1b93-49df-b7f8-7169db8efde0
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsWinNTSystemInfo, IADsWinNTSystemInfo interface [ADSI], IADsWinNTSystemInfo interface [ADSI],described, _ds_iadswinntsysteminfo, adsi.iadswinntsysteminfo, iads/IADsWinNTSystemInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsWinNTSystemInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsWinNTSystemInfo interface


## -description


The <b>IADsWinNTSystemInfo</b> interface  retrieves the WinNT system information about a computer. Such system information includes user account name, user domain, host name, and the primary domain controller of the host computer.

The <b>IADsWinNTSystemInfo</b> interface is implemented on the <b>WinNTSystemInfo</b> object residing in Activeds.dll, which is included in the standard installation of ADSI for domain-capable editions of Windows. You must explicitly create an instance of the <b>WinNTSystemInfo</b> object to call the methods on the <b>IADsWinNTSystemInfo</b> interface. This requirement means creating an <b>WinNTSystemInfo</b> instance with the  <a href="_com_cocreateinstance">CoCreateInstance</a> function in C/C++.

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




<a href="_com_cocreateinstance">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/5ba36851-3d03-4179-8cee-dbebe24b7c4e">IADsWinNTSystemInfo Property Methods</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

